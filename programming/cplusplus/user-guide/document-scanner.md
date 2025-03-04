---
layout: default-layout
title: User Guide for Document Scanner with C++
description: This is the user guide page of Document Scanner for C++ Language.
keywords: c++, user guide
---

# User Guide for Document Scanner with C++

In this guide, you will learn step by step on how to build a document scanner solution with Dynamsoft Capture Vision SDK using c++.

<span style="font-size:20px">Table of Contents</span>

- [User Guide for Document Scanner with C++](#user-guide-for-document-scanner-with-c)
  - [System Requirements](#system-requirements)
  - [Installation](#installation)
  - [Build Your Own Application](#build-your-own-application)
    - [Create A New Project](#create-a-new-project)
      - [For Windows](#for-windows)
      - [For Linux](#for-linux)
    - [Include the Library](#include-the-library)
    - [Initialize a Capture Vision Router Instance](#initialize-a-capture-vision-router-instance)
    - [Detect and Save the Normalized Document](#detect-and-save-the-normalized-document)
    - [Release the Allocated Memory](#release-the-allocated-memory)
    - [Build and Run the Project](#build-and-run-the-project)
      - [On Windows](#on-windows)
      - [On Linux](#on-linux)

## System Requirements

To find out whether your environment is supported, please read the [System Requirements]({{ site.dcvb_cpp }}index.html#system-requirements).

## Installation

If you haven't downloaded the SDK yet, <a href="https://download2.dynamsoft.com/dcv/dynamsoft-capture-vision-cpp-2.6.1000.241126.zip" target="_blank">download the `C/C++ Package`</a> now and unpack the package into a directory of your choice.

> For this tutorial, we unpack it to a pseudo directory `[INSTALLATION FOLDER]`, change it to your unpacking path for the following content.

## Build Your Own Application

In this section, we'll walk through the key steps needed to build an application that capture a document from an image file.

>You can download the complete source code from [here](https://github.com/Dynamsoft/capture-vision-cpp-samples/tree/main/Samples/DocumentScanner).

### Create A New Project

#### For Windows

1. Open Visual Studio. Go to File > New > Project, select Empty App and enter `DocumentScanner` in the `name` text box.

2. Add a new source file named `DocumentScanner.cpp` into the project.

#### For Linux

1. Create a new source file named `DocumentScanner.cpp` and place it into the folder `[INSTALLATION FOLDER]\Samples\DocumentScanner`.

2. Create a file named `Makefile` and put it in the same directory as the file `DocumentScanner.cpp`. The content of `Makefile` is as follows:

    ```makefile
    CC=gcc
    CCFLAGS=-c -std=c++11

    DS_LIB_PATH=[INSTALLATION FOLDER]/Dist/Lib/Linux/x64
    LDFLAGS=-L $(DS_LIB_PATH) -Wl,-rpath=$(DS_LIB_PATH) -Wl,-rpath=./
    DS_LIB=-lDynamsoftCaptureVisionRouter -lDynamsoftCore -lDynamsoftLicense -lDynamsoftUtility
    DS_JSON_PATH=[INSTALLATION FOLDER]/Dist/Templates

    STDLIB=-lstdc++

    TARGET=DocumentScanner
    OBJECT=DocumentScanner.o
    SOURCE=DocumentScanner.cpp

    # build rule for target.
    $(TARGET): $(OBJECT)
        $(CC) -o $(TARGET) $(OBJECT) $(STDLIB) $(DS_LIB) $(LDFLAGS)
        cp -r $(DS_JSON_PATH) $(DS_LIB_PATH)

    # target to build an object file
    $(OBJECT): $(SOURCE)
        $(CC) $(CCFLAGS) $(SOURCE)

    # the clean target
    .PHONY : clean
    clean: 
        rm -f $(OBJECT) $(TARGET) -r $(DS_LIB_PATH)/Templates
    ```

    >Note: The variable `DS_LIB_PATH` should be set to the correct directory where the library files are located. 

### Include the Library

1. Add headers and libs in `DocumentScanner.cpp`.

    ```cpp
    #include <iostream>
    #include <string>
    #include "[INSTALLATION FOLDER]/Include/DynamsoftCaptureVisionRouter.h"
    #include "[INSTALLATION FOLDER]/Include/DynamsoftUtility.h"

    using namespace std;
    using namespace dynamsoft::cvr;
    using namespace dynamsoft::ddn;
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

### Initialize a Capture Vision Router Instance

1. Initialize the license key

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

    >Note:
    > The string "DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9" here is a free public trial license. Note that network connection is required for this license to work. When it expires, you can request a 30-day free trial license from the <a href="https://www.dynamsoft.com/customer/license/trialLicense?utm_source=guide&product=dcv&package=c_cpp" target="_blank">Customer Portal</a>.

2. Create an instance of Dynamsoft Capture Vision Router

    ```cpp
    CCaptureVisionRouter* router = new CCaptureVisionRouter();
    ```

### Detect and Save the Normalized Document

1. Apply detection and normalization for an image file.

    ```cpp
    string imageFile = "[PATH-TO-THE-IMAGE-FILE]";
    CCapturedResult* result = router->Capture(imageFile.c_str(), CPresetTemplate::PT_DETECT_AND_NORMALIZE_DOCUMENT);
    ```

    > Please change the `[PATH-TO-THE-IMAGE-FILE]` to a real image file path.

2. Save the normalized result as an image file

    ```cpp
    cout << "File: " << imageFile << endl;
    if (result->GetErrorCode() != 0) {
        cout << "Error: " << result->GetErrorCode() << "," << result->GetErrorString() << endl;
    }
    CProcessedDocumentResult *processedDocumentResult = result->GetProcessedDocumentResult();
    if (processedDocumentResult == nullptr || processedDocumentResult->GetDeskewedImageResultItemsCount() == 0)
    {
        cout << "No document found." << endl;
    }
    else
    {
        int count = processedDocumentResult->GetDeskewedImageResultItemsCount();
        cout << "Deskewed " << count << " documents" << endl;
        for (int i = 0; i < count; i++)
        {
            const CDeskewedImageResultItem *deskewedImage = processedDocumentResult->GetDeskewedImageResultItem(i);
            string outPath = "deskewedResult_";
            outPath += to_string(i) + ".png";

            CImageIO imageIO;

            // 5.Save deskewed image to file.
            errorCode = imageIO.SaveToFile(deskewedImage->GetImageData(), outPath.c_str());
            if (errorCode == 0)
            {
                cout << "Document " << i << " file: " << outPath << endl;
            }
        }
    }
    ```

### Release the Allocated Memory

```cpp
if (processedDocumentResult)
	processedDocumentResult->Release();
if (result)
	result->Release();
delete router, router = NULL;   
```

### Build and Run the Project

#### On Windows

1. Build the application through Visual Studio.

2. Copy the following items from `[INSTALLATION FOLDER]\Dist` to the same folder as the EXE file. 
   
   - All the DLL files from `.\Lib\Windows\[PLATFORMS]`
   - Folder `Templates`

3. Run the program `DocumentScanner.exe`.

#### On Linux

1. Open a terminal and change to the target directory where `Makefile` located in. Build the sample:

    ```sh
    >make
    ```

2. Run the program `DocumentScanner`.

    ```sh
    >./DocumentScanner
    ```


> Note:
> 
> Please change all `[INSTALLATION FOLDER]` in above code snippet to your unpacking path.
