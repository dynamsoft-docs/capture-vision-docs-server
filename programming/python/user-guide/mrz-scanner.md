---
layout: default-layout
title: User Guide for MRZ Scanner with Python
description: This is the user guide page of MRZ Scanner for python.
keywords: user guide, mrz scanner, python
---

# User Guide for MRZ Scanner with Python

In this guide, you will learn step by step on how to build a MRZ scanner solution with Dynamsoft Capture Vision SDK using python.

- [User Guide for MRZ Scanner with Python](#user-guide-for-mrz-scanner-with-python)
  - [About the Solution](#about-the-solution)
  - [System Requirements](#system-requirements)
  - [Installation](#installation)
  - [Build Your Own Application](#build-your-own-application)
    - [Create a New Project](#create-a-new-project)
    - [Include the Library](#include-the-library)
    - [Initialize the License Key](#initialize-the-license-key)
    - [Create a CaptureVisionRouter Instance](#create-a-capturevisionrouter-instance)
    - [Invoke the Capturing](#invoke-the-capturing)
    - [Filter and Get MRZ Details](#filter-and-get-mrz-details)
    - [Build and Run the Project](#build-and-run-the-project)


## About the Solution

With the MRZ Scanner, you can extract the MRZ string from an image of a passport, visa, or ID card, and then parse it to retrieve data such as the first name, last name, document number, nationality, date of birth, expiration date, and personal number, converting them into human-readable fields.

## System Requirements

To find out whether your environment is supported, please read the [System Requirements]({{ site.dcvb_python }}index.html#system-requirements).

## Installation

Start terminal or command prompt to run the following command:

```
pip install dynamsoft_capture_vision_bundle
```

## Build Your Own Application

In this section, we'll walk through the key steps needed to build an application that reads the machine-readable zone (MRZ) from an image file.

> You can <a href="https://github.com/Dynamsoft/capture-vision-python-samples/blob/main/Samples/mrz_scanner.py" target="_blank">download the entire source code from here</a>.

### Create a New Project

Create a new source file named `mrz_scanner.py`.

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

> The string "DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9" here is a free public trial license. Note that network connection is required for this license to work. When it expires, you can request a 30-day free trial license from the <a href="https://www.dynamsoft.com/customer/license/trialLicense?utm_source=guide&product=mrz&package=python" target="_blank">Customer Portal</a>.

### Create a CaptureVisionRouter Instance

```python
cvr_instance = CaptureVisionRouter()
```

### Invoke the Capturing

```python
result = cvr_instance.capture("[PATH-TO-THE-IMAGE-FILE]", "ReadPassportAndId")
```

> Please change the `[PATH-TO-THE-IMAGE-FILE]` to a real image file path.

### Filter and Get MRZ Details

```python
if result.get_error_code() != EnumErrorCode.EC_OK:
    print("Error:", result.get_error_code(), result.get_error_string())
parsed_result = result.get_parsed_result()
if parsed_result is None or parsed_result.get_items() == 0:
    print("No MRZ detected.")
else:
    items = parsed_result.get_items()
    print("Detected", len(items), "MRZ Result(s).")
    for index,item in enumerate(items):
        print("Result", index+1)
        print("DocumentType:", item.get_code_type())
        if item.get_field_value("passportNumber"):
            print("DocumentID:", item.get_field_value("passportNumber"))
        else:
            print("DocumentID:", item.get_field_value("documentNumber"))
        # get more field values
```

### Build and Run the Project

1. Save the ``mrz_scanner.py` file.
2. Start terminal or command prompt and change to the target directory where `mrz_scanner.py` located in.
3. Run the command

```
python mrz_scanner.py
```

4. You will see the output message in the console like

```
Detected 1 MRZ Result(s).
Result 1
DocumentType: XXX
DocumentID: XXX
```

