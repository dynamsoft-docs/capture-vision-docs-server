---
layout: default-layout
title: CaptureVisionRouter Single-File Processing - Dynamsoft Capture Vision C++ Edition API
description: This page introduces APIs related to "Single-File Processing" by the CCaptureVisionRouter class of the Dynamsoft Capture Vision C++ Edition.
keywords: capture vision, capture, image processing, api reference, C++, single-file
needAutoGenerateSidebar: true
needGenerateH3Content: false
breadcrumbText: CVR C++ Single-File Processing
permalink: /programming/cplusplus/api-reference/capture-vision-router/single-file-processing.html
---

# Capture Vision Router C++ API Reference - Single-File Processing

| API Name              | Description                                               |
| --------------------- | --------------------------------------------------------- |
| [capture()](#capture) | Process an image or file to derive important information. |

## Capture

Process an image or file to derive important information. It can optionally use a specified template for the capture.

```cpp
CCapturedResultArray* Capture(const char* filePath, const char* templateName="");
CCapturedResultArray* Capture(const unsigned char *fileBytes, int fileSize, const char* templateName="");
CCapturedResult* Capture(const CImageData* pImageData, const char* templateName="");
```

**Parameters**

`[in] filePath` Specifies the path of the file to process.

`[in] templateName` Specifies the template to use for capturing. Default value is an empty string which means the factory default template.

`[in] fileBytes` Specifies the memory location containing the image to be processed.

`[in] fileSize`  Specifies the size of the image in bytes.

`[in] pImageData` Specifies the image data to process.

**Return Value**

Returns a pointer to a `CCapturedResultArray` object containing the captured results.

**Code Snippet**

```cpp
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
CCaptureVisionRouter* router = new CCaptureVisionRouter();
CCapturedResultArray* results = router->Capture("path/to/file.png", "myTemplate");
delete router;
```
