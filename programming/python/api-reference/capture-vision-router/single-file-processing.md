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
| [`capture_multi_pages`](#capture_multi_pages) | Processes an image or file containing multiple pages to derive important information. |

## capture

Process an image or file to derive important information. It can optionally use a specified template for the capture.

```python
def capture(self, *args) -> CapturedResult:
```

**Parameters**

`args` <*tuple*>: A variable-length argument list. Can be one of the following:

- `file_path` <*str*>, `template_name` <*str*, optional>: Specifies the path of the file to process and a `CaptureVisionTemplate` to use for capturing.
- `file_bytes` <*bytes*>, `template_name` <*str*, optional>: Specifies the image file bytes in memory to process and a `CaptureVisionTemplate` to use for capturing.
- `image_data` <*ImageData*>, `template_name` <*str*, optional>: Specifies the image data to process and a `CaptureVisionTemplate` to use for capturing.
- `image` <*numpy.ndarray*>, `image_pixel_format` <*EnumImagePixelFormat*, optional>, `template_name` <*str*, optional>: Specifies the image, formated in `numpy.ndarray`, and the image pixel format used in the image byte array to process and a `CaptureVisionTemplate` to use for capturing.

**Remarks**

- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_python_api }}capture-vision-router/enum-preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [InitSettings]({{ site.dcvb_python_api }}capture-vision-router/settings.html#initsettings) / [InitSettingsFromFile]({{ site.dcvb_python_api }}capture-vision-router/settings.html#initsettingsfromfile).
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `InitSettings` / `InitSettingsFromFile` and pass his own settings.
- If parameter `template_name` is not specified, the preset one named 'Default' will be used. However, if the preset ones have been overwritten as described above, the first `CaptureVisionTemplate` from the user's own settings will be used instead.

**Return Value**

Returns a `CapturedResult` object containing the captured items.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)

[EnumImagePixelFormat]({{ site.dcvb_python_api }}core/enum-image-pixel-format.html?lang=python)

[CapturedResult]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/captured-result.html)

## capture_multi_pages

Processes an image or file containing multiple pages to derive important information. It can optionally use a specified template for the capture.

```python
def capture_multi_pages(self, file: Union[str, bytes], template_name: str = "") -> CapturedResultArray:
```

**Parameters**

- `file` <*Union[str, bytes]*>: The input file containing multiple pages. It can be:
  - A file path <*str*> pointing to a multi-page image (e.g., PDF, TIFF).
  - A byte stream <*bytes*> representing the file content.
- `template_name` <*str*, optional>: Specifies a `CaptureVisionTemplate` to use for capturing.

**Remarks**

- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_python_api }}capture-vision-router/enum-preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [InitSettings]({{ site.dcvb_python_api }}capture-vision-router/settings.html#initsettings) / [InitSettingsFromFile]({{ site.dcvb_python_api }}capture-vision-router/settings.html#initsettingsfromfile).
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `InitSettings` / `InitSettingsFromFile` and pass his own settings.
- If parameter `template_name` is not specified, the preset one named 'Default' will be used. However, if the preset ones have been overwritten as described above, the first `CaptureVisionTemplate` from the user's own settings will be used instead.

**Return Value**

Returns a `CapturedResultArray` object containing a collection of captured results, where each entry corresponds to a processed page.

**See Also**

[CapturedResultArray]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/captured-result-array.html)
