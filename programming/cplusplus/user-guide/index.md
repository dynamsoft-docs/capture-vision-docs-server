---
layout: default-layout
title: C++ User Guide - Dynamsoft Capture Vision
description: This is the user guide page of Dynamsoft Capture Vision for C++ Language.
keywords: c++, user guide
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /programming/cplusplus/user-guide/index.html
---

# User Guide - C++

In this guide, you will learn step by step on how to build a barcode reader, label recognizer and document normalizer application with Dynamsoft Capture Vision SDK using C++ language.

> Read more on [Dynamsoft Capture Vision Features]({{site.introduction}})

<span style="font-size:20px">Table of Contents</span>

- [User Guide - C++](#user-guide---c)
  - [Requirements](#requirements)
  - [Installation](#installation)
  - [Build Your First Application](#build-your-first-application)
    - [Create A New Project](#create-a-new-project)
      - [For Windows](#for-windows)
      - [For Linux](#for-linux)
    - [Include the Library](#include-the-library)
    - [Initialize a Capture Vision Router Instance](#initialize-a-capture-vision-router-instance)
    - [Capture and Output Captured Results](#capture-and-output-captured-results)
    - [Release the Allocated Memory](#release-the-allocated-memory)
    - [Build and Run the Project](#build-and-run-the-project)
      - [On windows](#on-windows)
      - [On Linux](#on-linux)
  - [Process Multiple Images](#process-multiple-images)
    - [Preparation Steps](#preparation-steps)
    - [Add an Image Source as the Input](#add-an-image-source-as-the-input)
    - [Add Captured Result Receiver](#add-captured-result-receiver)
    - [Start Capturing](#start-capturing)
    - [Release Allocated Memory](#release-allocated-memory)
    - [Build and Run the Project Again](#build-and-run-the-project-again)

## Requirements

- Windows:
  - Supported Versions: Windows 7 and higher, or Windows Server 2003 and higher
  - Architecture: x64 and x86
  - Development Environment: Visual Studio 2012 or higher.

- Linux:
  - Supported Distributions: Ubuntu 14.04.4+ LTS, Debian 8+, CentOS 6+
  - Architectures: x64 (arm 32-bit and arm 64-bit coming soon)
  - Minimum GLIBC Version: GLIBC_2.18 or higher
  - Compiler: G++ 5.4 or higher

## Installation

If you haven't downloaded the SDK yet, <a href="https://download2.dynamsoft.com/dcv/dynamsoft-capture-vision-cpp-2.0.20.zip" target="_blank">download the `C/C++ Package`</a> now and unpack the package into a directory of your choice.

> For this tutorial, we unpack it to a pseudo directory `[INSTALLATION FOLDER]`, change it to your unpacking path for the following content.

## Build Your First Application

Let's start by creating a console application which demonstrates the minimum code needed to capture content from an image file.

>You can download the complete source code from [here](https://github.com/Dynamsoft/capture-vision-cpp-samples/tree/main/samples/HelloWorld/CaptureFromAnImage).

### Create A New Project

#### For Windows

1. Open Visual Studio. Go to File > New > Project, select Empty App and enter `CaptureFromAnImage` in the `name` text box.

2. Add a new source file named `CaptureFromAnImage.cpp` into the project.

#### For Linux

1. Create a new source file named `CaptureFromAnImage.cpp` and place it into the folder `[INSTALLATION FOLDER]\Resources\CaptureVision\Samples\HelloWorld\CaptureFromAnImage`.

2. Create a file named `Makefile` and put it in the same directory as the file `CaptureFromAnImage.cpp`. The content of `Makefile` is as follows:

    ```makefile
    CC=gcc
    CCFLAGS=-c -std=c++11

    DLRMODEL_PATH=[INSTALLATION FOLDER]/Distributables/CharacterModel
    DS_LIB_PATH=[INSTALLATION FOLDER]/Distributables/Lib/Linux/x64
    LDFLAGS=-L $(DS_LIB_PATH) -Wl,-rpath=$(DS_LIB_PATH) -Wl,-rpath=./
    DS_LIB=-lDynamsoftCaptureVisionRouter -lDynamsoftCore -lDynamsoftLicense -lDynamsoftUtility

    STDLIB=-lstdc++

    TARGET=CaptureFromAnImage
    OBJECT=CaptureFromAnImage.o
    SOURCE=CaptureFromAnImage.cpp

    # build rule for target.
    $(TARGET): $(OBJECT)
        $(CC) -o $(TARGET) $(OBJECT) $(STDLIB) $(DS_LIB) $(LDFLAGS)
        cp -r $(DLRMODEL_PATH) $(DS_LIB_PATH)

    # target to build an object file
    $(OBJECT): $(SOURCE)
        $(CC) $(CCFLAGS) $(SOURCE)

    # the clean target
    .PHONY : clean
    clean: 
        rm -f $(OBJECT) $(TARGET) -r $(DS_LIB_PATH)/CharacterModel
    ```

    >Note: The variable `DLRMODEL_PATH` and `DS_LIB_PATH` should be set to the correct directory where the library files are located. 

### Include the Library

1. Add headers and libs in `CaptureFromAnImage.cpp`.

    ```cpp
    #include <iostream>
    #include <string>
    #include "[INSTALLATION FOLDER]/Include/DynamsoftCaptureVisionRouter.h"

    using namespace std;
    using namespace dynamsoft::cvr;
    using namespace dynamsoft::dlr;
    using namespace dynamsoft::dbr;
    using namespace dynamsoft::ddn;
    using namespace dynamsoft::license;
    using namespace dynamsoft::utility;

    // The following code only applies to Windows.
    #if defined(_WIN64) || defined(_WIN32)
        #ifdef _WIN64
            #pragma comment(lib, "[INSTALLATION FOLDER]/Distributables/Lib/Windows/x64/DynamsoftCaptureVisionRouterx64.lib")
            #pragma comment(lib, "[INSTALLATION FOLDER]/Distributables/Lib/Windows/x64/DynamsoftCorex64.lib")
            #pragma comment(lib, "[INSTALLATION FOLDER]/Distributables/Lib/Windows/x64/DynamsoftLicensex64.lib")
            #pragma comment(lib, "[INSTALLATION FOLDER]/Distributables/Lib/Windows/x64/DynamsoftUtilityx64.lib")
        #else
            #pragma comment(lib, "[INSTALLATION FOLDER]/Distributables/Lib/Windows/x86/DynamsoftCaptureVisionRouterx86.lib")
            #pragma comment(lib, "[INSTALLATION FOLDER]/Distributables/Lib/Windows/x86/DynamsoftCorex86.lib")
            #pragma comment(lib, "[INSTALLATION FOLDER]/Distributables/Lib/Windows/x86/DynamsoftLicensex86.lib")
            #pragma comment(lib, "[INSTALLATION FOLDER]/Distributables/Lib/Windows/x86/DynamsoftUtilityx86.lib")
        #endif
    #endif
    ```

### Initialize a Capture Vision Router Instance

1. Initialize the license key

    ```cpp
    char error[512];
    
    CLicenseManager::InitLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9", error, 512);
    cout << "License initialization: " << error << endl;
    ```

    >Note:
    >
    >- An internet connection is required for the license to work.
    >- "DLS2***" is a default free public trial license used in the sample.
    >- If the license has expired, please request an extension through the <a href="https://www.dynamsoft.com/customer/license/trialLicense?utm_source=docs" target="_blank">customer portal</a>.

2. Create an instance of Dynamsoft Capture Vision Router

    ```cpp
    CCaptureVisionRouter* router = new CCaptureVisionRouter();
    ```

### Capture and Output Captured Results

1. Capture content from an image file

    ```cpp
    string imageFile = "[INSTALLATION FOLDER]/Resources/CaptureVision/Images/dcv-sample-image.png";
    CCapturedResult* result = router->Capture(imageFile.c_str(), CPresetTemplate::PT_DEFAULT);
    ```

2. Output the captured results

    ```cpp
    cout << "File: " << imageFile << endl;

    // 4.Outputs the result.
    if (result->GetErrorCode() != 0) {
        cout << "Error: " << result->GetErrorCode() << "," << result->GetErrorString() << endl;
    }

    /*
    * There can be multiple types of result items per image.
    */
    int count = result->GetItemsCount();
    cout << "Captured " << count << " items" << endl;
    for (int i = 0; i < count; i++) {
        const CCapturedResultItem* item = result->GetItem(i);

        CapturedResultItemType type = item->GetType();
        if (type == CapturedResultItemType::CRIT_BARCODE) {
            const CBarcodeResultItem* barcode = dynamic_cast<const CBarcodeResultItem*>(item);

            // Output the decoded barcode text.
            cout << ">>Item " << i << ": " << "Barcode," << barcode->GetText() << endl;
        }
        else if (type == CapturedResultItemType::CRIT_TEXT_LINE) {
            const CTextLineResultItem* textLine = dynamic_cast<const CTextLineResultItem*>(item);

            // Output the recognized text line.
            cout << ">>Item " << i << ": " << "TextLine," << textLine->GetText() << endl;
        }
        else if (type == CapturedResultItemType::CRIT_NORMALIZED_IMAGE) {
            const CNormalizedImageResultItem* normalizedImage = dynamic_cast<const CNormalizedImageResultItem*>(item);

            string outPath = "normalizedResult_";
            outPath += to_string(i) + ".png";

            CImageManager manager;

            // Save normalized iamge to file.
            errorcode = manager.SaveToFile(normalizedImage->GetImageData(), outPath.c_str());
            if (errorcode == 0) {
                cout << ">>Item " << i << ": " << "NormalizedImage," << outPath << endl;
            }
        }
    }
    ```

> Note:
> 
> Please change all `[INSTALLATION FOLDER]` in above code snippet to your unpacking path.

### Release the Allocated Memory

```cpp
delete router, router = NULL;
delete result, result = NULL;   
```

### Build and Run the Project

#### On windows

1. Build the application through Visual Studio.

2. Copy the related DLL files to the same folder as the EXE file. The DLL files can be found in `[INSTALLATION FOLDER]\Distributables\Lib\Windows\[platforms]`
    >Note: Select the corresponding folder (x86 or x64) based on your project's platform setting.

3. Copy the `[INSTALLATION FOLDER]\Distributables\CharacterModel` directory to the same folder as the EXE file.

4. Run the program `CaptureFromAnImage.exe`.

#### On Linux

1. Open a terminal and change to the target directory where `Makefile` located in. Build the sample:

    ```sh
    >make
    ```

2. Run the program `CaptureFromAnImage`.

    ```sh
    >./CaptureFromAnImage
    ```

## Process Multiple Images

If you need to process multiple images at once instead of one image, you can follow these steps:

### Preparation Steps

1. [Create a new project](#create-a-new-project) named `CaptureFromMultipleImages`.
2. [Initialize a Capture Vision Router Instance](#initialize-a-capture-vision-router-instance).
3. [Include the Library](#include-the-library).

>You can download the complete source code from [here](https://github.com/Dynamsoft/capture-vision-cpp-samples/tree/main/samples/HelloWorld/CaptureFromMultipleImages).

### Add an Image Source as the Input

The class `CDirectoryFetcher` is capable of converting a local directory to an image source. We will use it to connect multiple images to the image-processing engine.

1. Setting up a directory fetcher to retrieve image data sources from a directory.

    ```cpp
    CDirectoryFetcher *dirFetcher = new CDirectoryFetcher;
    dirFetcher->SetDirectory("[Your Image Path]");

    router->SetInput(dirFetcher);
    ```

2. Create a class `MyImageSourceStateListener` to implement the `CImageSourceStateListenter` interface, and call `StopCapturing` in the callback function.

    ```cpp
    class MyImageSourceStateListener : public CImageSourceStateListener
    {
    private:
        CCaptureVisionRouter* m_router;

    public:
        MyImageSourceStateListener(CCaptureVisionRouter* router) {
            m_router = router;
        }

        virtual void OnImageSourceStateReceived(ImageSourceState state)
        {
            if(state == ISS_EXHAUSTED)
                m_router->StopCapturing();
        }
    };
    ```

4. Register the `MyImageSourceStateListener` object to monitor the status of the image source.

    ```cpp
    CImageSourceStateListener *listener = new MyImageSourceStateListener(router);
    router->AddImageSourceStateListener(listener);
    ```

### Add Captured Result Receiver

1. Create a class `MyResultReceiver` to implement the `CCapturedResultReceiver` interface, and get the captured results in `OnCapturedResultReceived` callback function.

    ```cpp
    class MyResultReceiver : public CCapturedResultReceiver
    {
    public:
        virtual void OnCapturedResultReceived(CCapturedResult* pResult)
        {
            const CFileImageTag *tag = dynamic_cast<const CFileImageTag*>(pResult->GetOriginalImageTag());

            cout << "File: " << tag->GetFilePath() << endl;
            cout << "Page: " << tag->GetPageNumber() << endl;

            if (pResult->GetErrorCode() != EC_OK)
            {
                cout << "Error: " << pResult->GetErrorString() << endl;
            }
            else
            {
                int lCount = pResult->GetItemsCount();
                cout << "Captured " << lCount << " items" << endl;
                for (int i = 0; i < lCount; i++) {
                    const CCapturedResultItem* item = pResult->GetItem(i);

                    CapturedResultItemType type = item->GetType();
                    if (type == CapturedResultItemType::CRIT_BARCODE) {
                        const CBarcodeResultItem* barcode = dynamic_cast<const CBarcodeResultItem*>(item);

                        // Output the decoded barcode text.
                        cout << ">>Item " << i << ": " << "Barcode," << barcode->GetText() << endl;
                    }
                    else if (type == CapturedResultItemType::CRIT_TEXT_LINE) {
                        const CTextLineResultItem* textLine = dynamic_cast<const CTextLineResultItem*>(item);

                        // Output the recognized text line.
                        cout << ">>Item " << i << ": " << "TextLine," << textLine->GetText() << endl;
                    }
                    else if (type == CapturedResultItemType::CRIT_NORMALIZED_IMAGE) {
                        const CNormalizedImageResultItem* normalizedImage = dynamic_cast<const CNormalizedImageResultItem*>(item);

                        string outPath = "normalizedResult_";
                        outPath += to_string(i) + ".png";

                        CImageManager manager;

                        // Save normalized iamge to file.
                        int errorcode = manager.SaveToFile(normalizedImage->GetImageData(), outPath.c_str());
                        if (errorcode == 0) {
                            cout << ">>Item " << i << ": " << "NormalizedImage," << outPath << endl;
                        }
                    }
                }
            }

            cout << endl;
        }
    };
    ```

    >For the error handling mechanism, the SDK returns Error Code in the `CCapturedResult` object. You can add error handling code as needed. See [Error Code]({{site.dcv_enumerations}}core/error-code.html?src=cpp&&lang=cpp) for a full list of supported error codes.

2. Register the `MyResultReceiver` object to monitor the captured results of the router.

    ```cpp
    CCapturedResultReceiver* recv = new MyResultReceiver();
    router->AddResultReceiver(recv);
    ```

### Start Capturing

1. Start Capturing with the default Capture Vision Template.

    ```cpp
    router->StartCapturing(CPresetTemplate::PT_DEFAULT, true);
    ```

   >Note:
    >
    >- During the process, the callback function `OnCapturedResultReceived()` is triggered each time an image finishes processing. After all images are processed, the listener function `OnImageSourceStateReceived()` will return the image source state as `ISS_EXHAUSTED` and the process is stopped with the method `StopCapturing()`.

### Release Allocated Memory

```cpp
delete router, router = NULL;
delete dirFetcher, dirFetcher = NULL;
delete listener, listener = NULL;
delete recv, recv = NULL;
```

### Build and Run the Project Again

Please refer to [Build and Run the Project](#build-and-run-the-project).
