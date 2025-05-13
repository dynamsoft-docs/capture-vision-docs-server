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
| [`CaptureMultiPages`](#capturemultipages) | Processes an image or file containing multiple pages to derive important information. |

## Capture

Process an image or file to derive important information. It can optionally use a specified template for the capture.

```csharp
CapturedResult Capture(string filePath, string templateName="");
CapturedResult Capture(byte[] fileBytes, string templateName="");
CapturedResult Capture(ImageData imageData, string templateName="");
```

**Parameters**

`[in] filePath` Specifies the path of the file to process.

`[in] templateName` Specifies a `CaptureVisionTemplate` to use for capturing.

`[in] fileBytes` Specifies the image file bytes in memory to be processed.

`[in] imageData` Specifies the image data to process.

**Remarks**

- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [InitSettings]({{ site.dcvb_dotnet_api }}capture-vision-router/settings.html#initsettings) / [InitSettingsFromFile]({{ site.dcvb_dotnet_api }}capture-vision-router/settings.html#initsettingsfromfile).
- When using a custom template, the parameter `templateName` should be the name of the [`CaptureVisionTemplate` object]({{ site.dcvb_parameters }}file/capture-vision-template.html) in the JSON template file.
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `InitSettings` / `InitSettingsFromFile` and pass his own settings.
- If parameter `templateName` is not specified, the preset one named 'Default' will be used. However, if the preset ones have been overwritten as described above, the first `CaptureVisionTemplate` from the user's own settings will be used instead.

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

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)

## CaptureMultiPages

Processes an image or file containing multiple pages to derive important information.

```csharp
CapturedResult[] CaptureMultiPages(string filePath, string templateName = "");
CapturedResult[] CaptureMultiPages(byte[] fileBytes, string templateName = "")
```

**Parameters**

`[in] filePath` Specifies the path of the file to process.

`[in] templateName` Specifies a `CaptureVisionTemplate` to use for capturing.

`[in] fileBytes` Specifies the memory location containing the image to be processed.

**Remarks**

- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [InitSettings]({{ site.dcvb_dotnet_api }}capture-vision-router/settings.html#initsettings) / [InitSettingsFromFile]({{ site.dcvb_dotnet_api }}capture-vision-router/settings.html#initsettingsfromfile).
- When using a custom template, the parameter `templateName` should be the name of the [`CaptureVisionTemplate` object]({{ site.dcvb_parameters }}file/capture-vision-template.html) in the JSON template file.
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `InitSettings` / `InitSettingsFromFile` and pass his own settings.
- If parameter `templateName` is not specified, the preset one named 'Default' will be used. However, if the preset ones have been overwritten as described above, the first `CaptureVisionTemplate` from the user's own settings will be used instead.

**Return Value**

Returns an array of  `CapturedResult` objects containing the captured items.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |
| EC_FILE_NOT_FOUND | -10005 | The file is not found. |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |


**See Also**

[ImageData]({{ site.dcvb_dotnet_api }}core/basic-classes/image-data.html)
[CapturedResult]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/captured-result.html)
