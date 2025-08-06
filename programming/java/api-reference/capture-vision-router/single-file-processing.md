---
layout: default-layout
title: CaptureVisionRouter Single-File Processing Methods - Dynamsoft Capture Vision Router Module Java Edition API Reference
description: Definition of CaptureVisionRouter class Single-File Processing Methods in Dynamsoft Capture Vision Router Module Java Edition.
keywords: capture vision, capture, image processing, api reference, java, single-file
needAutoGenerateSidebar: true
needGenerateH3Content: false
---

# Single-File Processing Methods - CaptureVisionRouter Class

| Method                | Description                                               |
| --------------------- | --------------------------------------------------------- |
| [`capture`](#capture) | Process an image or file to derive important information. |
| [`captureMultiPages`](#capturemultipages) | Processes an image or file containing multiple pages to derive important information. |

## capture

Process an image or file to derive important information. It can optionally use a specified template for the capture.

```java
public CapturedResult capture(String filePath)
public CapturedResult capture(String filePath, String templateName)
public CapturedResult capture(byte[] fileBytes)
public CapturedResult capture(byte[] fileBytes, String templateName)
public CapturedResult capture(ImageData pImageData)
public CapturedResult capture(ImageData pImageData, String templateName)
```

**Parameters**

`filePath` <*String*>: Specifies the path of the file to process.

`fileBytes` <*byte[]*>: Specifies the image file bytes in memory to process.

`pImageData` <*ImageData*>: Specifies the image data to process.

`templateName` <*String*, optional>: Specifies a `CaptureVisionTemplate` to use for capturing.

**Remarks**

- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_java_api }}capture-vision-router/enum-preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [initSettings]({{ site.dcvb_java_api }}capture-vision-router/settings.html#initsettings) / [initSettingsFromFile]({{ site.dcvb_java_api }}capture-vision-router/settings.html#initsettingsfromfile).
- When using a custom template, the parameter `templateName` should be the name of the [`CaptureVisionTemplate` object]({{ site.dcvb_parameters }}file/capture-vision-template.html) in the JSON template file.
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `initSettings` / `initSettingsFromFile` and pass his own settings.
- If parameter `templateName` is not specified, the preset one named 'Default' will be used. However, if the preset ones have been overwritten as described above, the first `CaptureVisionTemplate` from the user's own settings will be used instead.

**Return Value**

Returns a `CapturedResult` object containing the captured items.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

[CapturedResult]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/captured-result.html)

## captureMultiPages

Processes an image or file containing multiple pages to derive important information. It can optionally use a specified template for the capture.

```java
public CapturedResult[] captureMultiPages(String filePath)
public CapturedResult[] captureMultiPages(String filePath, String templateName)
public CapturedResult[] captureMultiPages(byte[] fileBytes)
public CapturedResult[] captureMultiPages(byte[] fileBytes, String templateName)
```

**Parameters**

`filePath` <*String*>: Specifies the path of the file containing multiple pages to process.

`fileBytes` <*byte[]*>: Specifies the image file bytes in memory containing multiple pages to process.

`templateName` <*String*, optional>: Specifies a `CaptureVisionTemplate` to use for capturing.

**Remarks**

- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_java_api }}capture-vision-router/enum-preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [initSettings]({{ site.dcvb_java_api }}capture-vision-router/settings.html#initsettings) / [initSettingsFromFile]({{ site.dcvb_java_api }}capture-vision-router/settings.html#initsettingsfromfile).
- When using a custom template, the parameter `templateName` should be the name of the [`CaptureVisionTemplate` object]({{ site.dcvb_parameters }}file/capture-vision-template.html) in the JSON template file.
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `initSettings` / `initSettingsFromFile` and pass his own settings.
- If parameter `templateName` is not specified, the preset one named 'Default' will be used. However, if the preset ones have been overwritten as described above, the first `CaptureVisionTemplate` from the user's own settings will be used instead.

**Return Value**

Returns an array of `CapturedResult` objects containing a collection of captured results, where each entry corresponds to a processed page.
