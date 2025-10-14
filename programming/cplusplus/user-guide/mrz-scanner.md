---
layout: default-layout
title: User Guide for MRZ Scanner with C++
description: This is the user guide page of MRZ Scanner for C++ Language.
keywords: c++, user guide
---

# User Guide for MRZ Scanner with C++

In this guide, you will learn step by step on how to build a MRZ Scanner solution with Dynamsoft Capture Vision SDK using c++.

<span style="font-size:20px">Table of Contents</span>

- [User Guide for MRZ Scanner with C++](#user-guide-for-mrz-scanner-with-c)
  - [About the Solution](#about-the-solution)
  - [System Requirements](#system-requirements)
  - [Installation](#installation)
  - [Build Your Own Application](#build-your-own-application)
    - [Create A New Project](#create-a-new-project)
      - [For Windows](#for-windows)
      - [For Linux](#for-linux)
    - [Include the Library](#include-the-library)
    - [Initialize the License Key](#initialize-the-license-key)
    - [Create a CaptureVisionRouter Instance](#create-a-capturevisionrouter-instance)
    - [Invoke the Capturing](#invoke-the-capturing)
    - [Filter and Get MRZ Details](#filter-and-get-mrz-details)
    - [Release the Allocated Memory](#release-the-allocated-memory)
    - [Build and Run the Project](#build-and-run-the-project)
      - [On Windows](#on-windows)
      - [On Linux](#on-linux)

## About the Solution

With the MRZ Scanner, you can extract the MRZ string from an image of a passport, visa, or ID card, and then parse it to retrieve data such as the first name, last name, document number, nationality, date of birth, expiration date, and personal number, converting them into human-readable fields.

## System Requirements

To find out whether your environment is supported, please read the [System Requirements]({{ site.dcvb_cpp }}index.html#system-requirements).

## Installation

If you haven't downloaded the SDK yet, <a href="https://download2.dynamsoft.com/dcv/dynamsoft-capture-vision-cpp-3.2.1000.251014.zip" target="_blank">download the `C/C++ Package`</a> now and unpack the package into a directory of your choice.

> [!IMPORTANT]
> For this tutorial, we unpack it to a pseudo directory `[INSTALLATION FOLDER]`, change it to your unpacking path for the following content.

## Build Your Own Application

In this section, we’ll walk through the key steps needed to build an application that reads the machine-readable zone (MRZ) from an image file.

> [!TIP]
>You can download the complete source code from [here](https://github.com/Dynamsoft/capture-vision-cpp-samples/tree/main/Samples/MRZScanner).

### Create A New Project

#### For Windows

1. Open Visual Studio. Go to File > New > Project, select Empty App and enter `MRZScanner` in the `name` text box.

2. Add a new source file named `MRZScanner.cpp` into the project.

#### For Linux

1. Create a new source file named `MRZScanner.cpp` and place it into the folder `[INSTALLATION FOLDER]\Samples\MRZScanner`.

2. Create a file named `Makefile` and put it in the same directory as the file `MRZScanner.cpp`. The content of `Makefile` is as follows:

    ```makefile
    CC=gcc
    CCFLAGS=-c -std=c++11

    DLRMODEL_PATH=../../Dist/Models
    DCPRES_PATH=../../Dist/ParserResources
    CONFUSABLE_CHARS_PATH=../../Dist/ConfusableChars.data
    OVERLAPPING_CHARS_PATH=../../Dist/OverlappingChars.data
    DS_JSON_PATH=../../Dist/Templates
    DS_LIB_PATH=../../Dist/Lib/Linux/x64
    LDFLAGS=-L $(DS_LIB_PATH) -Wl,-rpath=$(DS_LIB_PATH) -Wl,-rpath=./
    DS_LIB=-lDynamsoftCaptureVisionRouter -lDynamsoftCore -lDynamsoftUtility -lDynamsoftLicense

    STDLIB=-lstdc++

    TARGET=MRZScanner
    OBJECT=MRZScanner.o
    SOURCE=MRZScanner.cpp

    # build rule for target.
    $(TARGET): $(OBJECT)
        $(CC) -o $(TARGET) $(OBJECT) $(STDLIB) $(DS_LIB) $(LDFLAGS)
        cp -r $(DLRMODEL_PATH) $(DS_LIB_PATH)
        cp -r $(DCPRES_PATH) $(DS_LIB_PATH)
        cp $(CONFUSABLE_CHARS_PATH) $(DS_LIB_PATH)
        cp $(OVERLAPPING_CHARS_PATH) $(DS_LIB_PATH)
        cp -r $(DS_JSON_PATH) $(DS_LIB_PATH)

    # target to build an object file
    $(OBJECT): $(SOURCE)
        $(CC) $(CCFLAGS) $(SOURCE)

    # the clean target
    .PHONY : clean
    clean: 
        rm -f $(OBJECT) $(TARGET) $(DS_LIB_PATH)/ConfusableChars.data $(DS_LIB_PATH)/OverlappingChars.data -r $(DS_LIB_PATH)/Models $(DS_LIB_PATH)/ParserResources $(DS_LIB_PATH)/Templates
    ```

### Include the Library

Add headers and libs in `MRZScanner.cpp`.

```cpp
#include <iostream>
#include <string>
#include "[INSTALLATION FOLDER]/Include/DynamsoftCaptureVisionRouter.h"
#include "[INSTALLATION FOLDER]/Include/DynamsoftUtility.h"

using namespace std;
using namespace dynamsoft::cvr;
using namespace dynamsoft::dlr;
using namespace dynamsoft::dcp;
using namespace dynamsoft::license;
using namespace dynamsoft::utility;

// The following code only applies to Windows.
#if defined(_WIN64) || defined(_WIN32)
    #ifdef _WIN64
        #pragma comment(lib, "[INSTALLATION FOLDER]/Dist/Lib/Windows/x64/DynamsoftCaptureVisionRouterx64.lib")
        #pragma comment(lib, "[INSTALLATION FOLDER]/Dist/Lib/Windows/x64/DynamsoftCorex64.lib")
        #pragma comment(lib, "[INSTALLATION FOLDER]/Dist/Lib/Windows/x64/DynamsoftLicensex64.lib")
        #pragma comment(lib, "[INSTALLATION FOLDER]/Dist/Lib/Windows/x64/DynamsoftUtilityx64.lib")
    #else
        #pragma comment(lib, "[INSTALLATION FOLDER]/Dist/Lib/Windows/x86/DynamsoftCaptureVisionRouterx86.lib")
        #pragma comment(lib, "[INSTALLATION FOLDER]/Dist/Lib/Windows/x86/DynamsoftCorex86.lib")
        #pragma comment(lib, "[INSTALLATION FOLDER]/Dist/Lib/Windows/x86/DynamsoftLicensex86.lib")
        #pragma comment(lib, "[INSTALLATION FOLDER]/Dist/Lib/Windows/x86/DynamsoftUtilityx86.lib")
    #endif
#endif
```

### Initialize the License Key

If this is your first time using the library, you will need to obtain a trial license key. We recommend getting your own 30-day trial license through the following modal:

{% include trialLicense.html %}

Open the `MRZScanner.cpp` file and add the following code inside the `Main` method to initialize the license for using the SDK in the application:

```cpp
int errorcode = 0;
char error[512];
errorcode = CLicenseManager::InitLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9", error, 512);
if (errorcode != ErrorCode::EC_OK && errorcode != ErrorCode::EC_LICENSE_CACHE_USED)
{
    cout << "License initialization failed: ErrorCode: " << errorcode << ", ErrorString: " << error << endl;
}
else
{
    // codes from following steps...
}
```

> [!NOTE]
> The string "DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9" here is a free public trial license. Note that network connection is required for this license to work. Please replace it with your own 30-day trial license.

### Create a CaptureVisionRouter Instance

```cpp
CCaptureVisionRouter* router = new CCaptureVisionRouter();
```

### Invoke the Capturing

```cpp
string imageFile = "[PATH-TO-THE-IMAGE-FILE]";
CCapturedResult* result = router->Capture(imageFile.c_str(), "ReadPassportAndId");
```

> [!IMPORTANT]
> Please change the `[PATH-TO-THE-IMAGE-FILE]` to a real image file path.

### Filter and Get MRZ Details

```cpp
cout << "File: " << imageFile << endl;
if (result->GetErrorCode() != 0) {
    cout << "Error: " << result->GetErrorCode() << "," << result->GetErrorString() << endl;
}
CParsedResult* dcpResult = result->GetParsedResult();
if (dcpResult == NULL || dcpResult->GetItemsCount() == 0)
{
    cout << "No MRZ results." << endl;
}
else
{
    int lCount = dcpResult->GetItemsCount();
    cout << "Detected " << lCount << " MRZ Result(s)." << endl;
    for (int i = 0; i < lCount; i++)
    {
        const CParsedResultItem *item = dcpResult->GetItem(i);
        string docType = item->GetCodeType();
        cout << "DocumentType: " << docType << endl;
        if (docType == "MRTD_TD3_PASSPORT")
        {
            cout << "DocumentID: " << item->GetFieldValue("passportNumber") << endl;
        }
        else
        {
            cout << "DocumentID: " << item->GetFieldValue("documentNumber") << endl;
        }
        //get more field values
        //cout << "DocumentID: " << item->GetFieldValue("[FIELD-NAME]") << endl;
    }
}
```

### Release the Allocated Memory

```cpp
if (dcpResult)
    dcpResult->Release();
if (result)
    result->Release();
delete router, router = NULL;   
```

### Build and Run the Project

#### On Windows

1. Build the application through Visual Studio.

2. Copy the following items from `[INSTALLATION FOLDER]\Dist` to the same folder as the EXE file. 
   
   - All the DLL files from `.\Lib\Windows\[PLATFORMS]`
   - File `ConfusableChars.data`
   - File `OverlappingChars.data`
   - File `Models\MRZTextLineRecognition.data` (including folder `Models`)
   - File `Models\MRZCharRecognition.data` (including folder `Models`)
   - File `Templates\MRZScanner.json` (including folder `Templates`)
   - Folders `ParserResources`

3. Run the program `MRZScanner.exe`.

#### On Linux

1. Open a terminal and change to the target directory where `Makefile` located in. Build the sample:

    ```sh
    >make
    ```

2. Run the program `MRZScanner`.

    ```sh
    >./MRZScanner
    ```

> [!IMPORTANT]
> Please change all `[INSTALLATION FOLDER]` in above code snippet to your unpacking path.
