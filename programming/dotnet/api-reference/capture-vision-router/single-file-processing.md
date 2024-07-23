---
layout: default-layout
title: CaptureVisionRouter Single-File Processing Methods - Dynamsoft Capture Vision Router Module .NET Edition API Reference
description: Definition of CaptureVisionRouter class Single-File Processing Methods in Dynamsoft Capture Vision Router Module .NET Edition.
keywords: capture vision, capture, image processing, api reference, .NET, single-file
needAutoGenerateSidebar: true
needGenerateH3Content: false
---

# Single-File Processing Methods - CaptureVisionRouter Class

| Method                | Description                                               |
| --------------------- | --------------------------------------------------------- |
| [`Capture`](#capture) | Process an image or file to derive important information. |

## Capture

Process an image or file to derive important information. It can optionally use a specified template for the capture.

```csharp
CapturedResult Capture(string filePath, string templateName="");
CapturedResult Capture(byte[] fileBytes, string templateName="");
CapturedResult Capture(ImageData imageData, string templateName="");
```

**Parameters**

`[in] filePath` Specifies the path of the file to process.

`[in] templateName` Specifies the template to use for capturing. Default value is an empty string which means the factory default template.

`[in] fileBytes` Specifies the image file bytes in memory to be processed.

`[in] imageData` Specifies the image data to process.

**Return Value**

Returns a `CapturedResult` object containing the captured items.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |
| EC_FILE_NOT_FOUND | -10005 | The file is not found. |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_MULTI_PAGES_NOT_SUPPORTED | -10066 | The api does not support multi-page files. Please use FileFetcher instead. |

**See Also**

[ImageData]({{ site.dcv_dotnet_api }}core/basic-classes/image-data.html)
