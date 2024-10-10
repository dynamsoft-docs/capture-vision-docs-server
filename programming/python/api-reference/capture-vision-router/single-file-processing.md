---
layout: default-layout
title: CaptureVisionRouter Single-File Processing Methods - Dynamsoft Capture Vision Router Module Python Edition API Reference
description: Definition of CaptureVisionRouter class Single-File Processing Methods in Dynamsoft Capture Vision Router Module Python Edition.
keywords: capture vision, capture, image processing, api reference, python, single-file
needAutoGenerateSidebar: true
needGenerateH3Content: false
---

# Single-File Processing Methods - CaptureVisionRouter Class

| Method                | Description                                               |
| --------------------- | --------------------------------------------------------- |
| [`capture`](#capture) | Process an image or file to derive important information. |

## capture

Process an image or file to derive important information. It can optionally use a specified template for the capture.

```python
def capture(self, *args) -> CapturedResult:
```

**Parameters**

`args` <*tuple*>: A variable-length argument list. Can be one of the following:

- `file_path` <*str*>, `template_name` <*str*, optional>: Specifies the path of the file to process and the template to use for capturing.
- `file_bytes` <*bytes*>, `template_name` <*str*, optional>: Specifies the image file bytes in memory to process and the template to use for capturing.
- `image_data` <*ImageData*>, `template_name` <*str*, optional>: Specifies the image data to process and the template to use for capturing.

**Remarks**

Default value for `template_name` is an empty string which means the factory default template.

**Return Value**

Returns a `CapturedResult` object containing the captured items.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

[CapturedResult]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/captured-result.html)
