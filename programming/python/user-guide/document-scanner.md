---
layout: default-layout
title: User Guide for Document Scanner with Python
description: This is the user guide page of Document Scanner for Python Edition.
keywords: user guide, document scanner, python
---

# User Guide for Document Scanner with Python

In this guide, you will learn step by step on how to build a document scanner solution with Dynamsoft Capture Vision SDK using python.

- [User Guide for Document Scanner with Python](#user-guide-for-document-scanner-with-python)
  - [System Requirements](#system-requirements)
  - [Installation](#installation)
  - [Build Your Own Application](#build-your-own-application)
    - [Create a New Project](#create-a-new-project)
    - [Include the Library](#include-the-library)
    - [Initialize the License Key](#initialize-the-license-key)
    - [Create a CaptureVisionRouter Instance](#create-a-capturevisionrouter-instance)
    - [Detect and Save the Normalized Document](#detect-and-save-the-normalized-document)
    - [Build and Run the Project](#build-and-run-the-project)


## System Requirements

To find out whether your environment is supported, please read the [System Requirements]({{ site.dcvb_python }}index.html#system-requirements).

## Installation

Start terminal or command prompt to run the following command:

```
pip install dynamsoft_capture_vision_bundle
```

## Build Your Own Application

In this section, we'll walk through the key steps needed to build an application that capture a document from an image file.

> You can <a href="https://github.com/Dynamsoft/capture-vision-python-samples/blob/main/Samples/document_scanner.py" target="_blank">download the entire source code from here</a>.

### Create a New Project

Create a new source file named `document_scanner.py`.

### Include the Library

Import package `dynamsoft_capture_vision_bundle` in the source file.

```python
from dynamsoft_capture_vision_bundle import *
```

### Initialize the License Key

Add the following code inside the `__main__` method to initialize the license for using the SDK in the application:

```python
errorCode, errorMsg = LicenseManager.init_license("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9")
if errorCode != EnumErrorCode.EC_OK and errorCode != EnumErrorCode.EC_LICENSE_CACHE_USED:
    print("License initialization failed: ErrorCode:", errorCode, ", ErrorString:", errorMsg)
else:
    # codes from following steps
```

> The string "DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9" here is a free public trial license. Note that network connection is required for this license to work. When it expires, you can request a 30-day free trial license from the <a href="https://www.dynamsoft.com/customer/license/trialLicense?utm_source=guide&product=dcv&package=python" target="_blank">Customer Portal</a>.

### Create a CaptureVisionRouter Instance

```python
cvr = CaptureVisionRouter()
```

### Detect and Save the Normalized Document

1. Apply detection and normalization for an image file.

```python
result = cvr.capture("[PATH-TO-THE-IMAGE-FILE]", EnumPresetTemplate.PT_DETECT_AND_NORMALIZE_DOCUMENT.value)
```

> Please change the `[PATH-TO-THE-IMAGE-FILE]` to a real image file path.

2. Save the normalized result as an image file

```python
if result.get_error_code() != EnumErrorCode.EC_OK:
    print("Error:", result.get_error_code(), result.get_error_string())
normalized_images_result = result.get_normalized_images_result()
if normalized_images_result is None or len(normalized_images_result.get_items()) == 0:
    print("No document detected.")
else:
    items = normalized_images_result.get_items()
    print("Normalized", len(items), "documents.")
    for index,item in enumerate(normalized_images_result.get_items()):                   
        out_path = "normalizedResult_" + str(index) + ".png"
        image_manager = ImageManager()
        image = item.get_image_data()
        if image != None:
            errorCode, errorMsg = image_manager.save_to_file(image, out_path)
            if errorCode == 0:
                print("Document " + str(index) + " file: " + out_path)
```

### Build and Run the Project

1. Save the ``document_scanner.py` file.
2. Start terminal or command prompt and change to the target directory where `document_scanner.py` located in.
3. Run the command

```
python document_scanner.py
```

4. You will see the output message in the console like

```
Normalized 1 documents.
Document 0 file: XXX
```

