---
layout: default-layout
title: User Guide for Document Scanner with .NET
description: This is the user guide page of Document Scanner for .NET Edition.
keywords: user guide index, .NET
---

# User Guide for Document Scanner with .NET

In this guide, you will learn step by step on how to build a document scanner solution with Dynamsoft Capture Vision SDK using C#.

- [User Guide for Document Scanner with .NET](#user-guide-for-document-scanner-with-net)
  - [System Requirements](#system-requirements)
  - [Build Your Own Application](#build-your-own-application)
    - [Create a New Project](#create-a-new-project)
    - [Install the NuGet Package](#install-the-nuget-package)
    - [Import the Namespace](#import-the-namespace)
    - [Initialize the License Key](#initialize-the-license-key)
    - [Create a CaptureVisionRouter Instance](#create-a-capturevisionrouter-instance)
    - [Detect and Save the Normalized Document](#detect-and-save-the-normalized-document)
    - [Build and Run the Project](#build-and-run-the-project)

## System Requirements

To find out whether your environment is supported, please read the [System Requirements]({{ site.dcvb_dotnet }}index.html#system-requirements).

## Build Your Own Application

In this section, we'll walk through the key steps needed to build an application that capture a document from an image file.

> You can <a href="https://github.com/Dynamsoft/capture-vision-dotnet-samples/tree/main/Samples/DocumentScanner" target="_blank">download the entire source code from here</a>.

### Create a New Project

Start Visual Studio or your preferred C# IDE.

Create a new C# Console Application project. Let's name it `DocumentScanner`.

### Install the NuGet Package

In the Solution Explorer, right-click on your project and select Manage NuGet Packages.

Search for and install the `Dynamsoft.DotNet.CaptureVision.Bundle` nuget package.

### Import the Namespace

Open the `Program.cs` file and add the following namespaces.

```csharp
using Dynamsoft.CVR;
using Dynamsoft.License;
using Dynamsoft.Core;
using Dynamsoft.Utility;
using Dynamsoft.DDN;
```

### Initialize the License Key

Open the `Program.cs` file and add the following code inside the `Main` method to initialize the license for using the SDK in the application:

```csharp
int errorCode = 1;
string errorMsg;
errorCode = LicenseManager.InitLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9", out errorMsg);
if (errorCode != (int)EnumErrorCode.EC_OK && errorCode != (int)EnumErrorCode.EC_LICENSE_CACHE_USED)
    Console.WriteLine("License initialization error: " + errorMsg);
```

> The string "DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9" here is a free public trial license. Note that network connection is required for this license to work. When it expires, you can request a 30-day free trial license from the <a href="https://www.dynamsoft.com/customer/license/trialLicense?utm_source=guide&product=dcv&package=dotnet" target="_blank">Customer Portal</a>.

### Create a CaptureVisionRouter Instance

```csharp
using (CaptureVisionRouter cvRouter = new CaptureVisionRouter())
{
    //code for invoking the capturing
}
```

### Detect and Save the Normalized Document

1. Apply detection and normalization for an image file.

```csharp
using (CaptureVisionRouter cvRouter = new CaptureVisionRouter())
{
    string imageFile = "[PATH-TO-THE-IMAGE-FILE]";
    CapturedResult[] results = cvRouter.CaptureMultiPages(imageFile, PresetTemplate.PT_DETECT_AND_NORMALIZE_DOCUMENT)
    //code for saving the normalized result as an image file
}
```

> Please change the `[PATH-TO-THE-IMAGE-FILE]` to a real image file path.

2. Save the normalized result as an image file

```csharp
if (results == null || results.Length == 0)
{
    Console.WriteLine("No document detected.");
}
else
{
    for (int index = 0; index < results.Length; index++)
    {
        CapturedResult result = results[index];
        if (result.GetErrorCode() == (int)EnumErrorCode.EC_UNSUPPORTED_JSON_KEY_WARNING)
        {
            Console.WriteLine("Warning: " + result.GetErrorCode() + ", " + result.GetErrorString());
        }
        else if (result.GetErrorCode() != (int)EnumErrorCode.EC_OK)
        {
            Console.WriteLine("Error: " + result.GetErrorCode() + ", " + result.GetErrorString());
        }
        FileImageTag tag = result.GetOriginalImageTag() as FileImageTag;
        int pageNumber = tag != null ? tag.GetPageNumber() : index;
        ProcessedDocumentResult processedDocumentResult = result.GetProcessedDocumentResult();
        if (processedDocumentResult == null || processedDocumentResult.GetEnhancedImageResultItems().Length == 0)
        {
            Console.WriteLine("Page-" + (pageNumber + 1) + " No document found.");
        }
        else
        {
            EnhancedImageResultItem[] items = processedDocumentResult.GetEnhancedImageResultItems();
            for (int i = 0; i < items.Length; i++)
            {
                EnhancedImageResultItem enhancedResult = items[i];
                string outPath = "Page_" + (pageNumber + 1) + "enhancedResult_" + i + ".png";
                ImageIO imageIo = new ImageIO();
                var image = enhancedResult.GetImageData();
                if (image != null)
                {
                    errorCode = imageIo.SaveToFile(image, outPath);
                    if (errorCode == 0)
                    {
                        Console.WriteLine("Document " + i + " file: " + outPath);
                    }
                }
            }
        }
    }
}
```

### Build and Run the Project

Save the `Program.cs` file and then compile and run the program using your IDE (such as Visual Studio). You will see the output message in the console like

```
Normalized 1 documents.
Document 0 file: XXX
```
