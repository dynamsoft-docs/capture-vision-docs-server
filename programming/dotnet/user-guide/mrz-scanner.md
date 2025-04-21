---
layout: default-layout
title: .NET Edition User Guide Index
description: This is the user guide page of MRZ Scanner for .NET.
keywords: user guide index, .NET
---

# User Guide for MRZ Scanner with .NET

In this guide, you will learn step by step on how to build a MRZ scanner solution with Dynamsoft Capture Vision SDK using C#.

- [User Guide for MRZ Scanner with .NET](#user-guide-for-mrz-scanner-with-net)
  - [About the Solution](#about-the-solution)
  - [System Requirements](#system-requirements)
  - [Build Your Own Application](#build-your-own-application)
    - [Create a New Project](#create-a-new-project)
    - [Install the NuGet Package](#install-the-nuget-package)
    - [Import the Namespace](#import-the-namespace)
    - [Initialize the License Key](#initialize-the-license-key)
    - [Create a CaptureVisionRouter Instance](#create-a-capturevisionrouter-instance)
    - [Invoke the Capturing](#invoke-the-capturing)
    - [Filter and Get MRZ Details](#filter-and-get-mrz-details)
    - [Build and Run the Project](#build-and-run-the-project)

## About the Solution

With the MRZ Scanner, you can extract the MRZ string from an image of a passport, visa, or ID card, and then parse it to retrieve data such as the first name, last name, document number, nationality, date of birth, expiration date, and personal number, converting them into human-readable fields.

## System Requirements

To find out whether your environment is supported, please read the [System Requirements]({{ site.dcvb_dotnet }}index.html#system-requirements).

## Build Your Own Application

In this section, we'll walk through the key steps needed to build an application that reads the machine-readable zone (MRZ) from an image file.

> You can <a href="https://github.com/Dynamsoft/capture-vision-dotnet-samples/tree/main/Samples/MRZScanner" target="_blank">download the entire source code from here</a>.

### Create a New Project

Start Visual Studio or your preferred C# IDE.

Create a new C# Console Application project. Let's name it `MRZScanner`.

### Install the NuGet Package

In the Solution Explorer, right-click on your project and select Manage NuGet Packages.

Search for and install the `Dynamsoft.DotNet.CaptureVision.Bundle` nuget package.

### Import the Namespace

Open the `Program.cs` file and add the following namespaces.

```csharp
using Dynamsoft.Core;
using Dynamsoft.CVR;
using Dynamsoft.License;
using Dynamsoft.DCP;
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

> The string "DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9" here is a free public trial license. Note that network connection is required for this license to work. When it expires, you can request a 30-day free trial license from the <a href="https://www.dynamsoft.com/customer/license/trialLicense?utm_source=guide&product=mrz&package=dotnet" target="_blank">Customer Portal</a>.

### Create a CaptureVisionRouter Instance

```csharp
using (CaptureVisionRouter cvRouter = new CaptureVisionRouter())
{
    //code for invoking the capturing
}
```

### Invoke the Capturing

```csharp
using (CaptureVisionRouter cvRouter = new CaptureVisionRouter())
{
    string imageFile = "[PATH-TO-THE-IMAGE-FILE]";
    using (CapturedResult? result = cvRouter.Capture(imageFile, "ReadPassportAndId"))
    {
        //code for filtering and getting MRZ details
    }
}
```

> Please change the `[PATH-TO-THE-IMAGE-FILE]` to a real image file path.

### Filter and Get MRZ Details

```csharp
if (result == null)
{
    Console.WriteLine("No MRZ detected.");
}
else
{
    if (result.GetErrorCode() != 0)
    {
        Console.WriteLine("Error: " + result.GetErrorCode() + ", " + result.GetErrorString());
    }
    ParsedResult? parsedResult = result.GetParsedResult();
    if (parsedResult == null || parsedResult.GetItems().Length == 0)
    {
        Console.WriteLine("No MRZ results.");
    }
    else
    {
        ParsedResultItem[] items = parsedResult.GetItems();
        Console.WriteLine("Detected " + items.Length + " MRZ Result(s).");
        foreach (var item in items)
        {
            string? docType = item.GetCodeType();
            Console.WriteLine("DocumentType:" + docType);
            if (docType == "MRTD_TD3_PASSPORT")
            {
                Console.WriteLine("DocumentID:" + item.GetFieldValue("passportNumber"));
            }
            else
            {
                Console.WriteLine("DocumentID:" + item.GetFieldValue("documentNumber"));
            }
            //get more field values
            //Console.WriteLine(item.GetFieldValue("[FIELD-NAME]"));
        }
    }
}
```

### Build and Run the Project

Save the `Program.cs` file and then compile and run the program using your IDE (such as Visual Studio). You will see the output message in the console like

```
Detected 1 MRZ Result(s).
DocumentType: XXX
DocumentID: XXX
```
