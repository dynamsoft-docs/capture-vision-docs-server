---
layout: default-layout
title: CaptureVisionRouter Single-File Processing - Dynamsoft Capture Vision C++ Edition API
description: This page introduces APIs related to Single-File Processing by the CCaptureVisionRouter class of the Dynamsoft Capture Vision C++ Edition.
keywords: capture vision, capture, image processing, api reference, C++, single-file
needAutoGenerateSidebar: true
needGenerateH3Content: false
breadcrumbText: CVR C++ Single-File Processing
---

# Single-File Processing

| API Name              | Description                                               |
| --------------------- | --------------------------------------------------------- |
| [`Capture`](#capture) | Process an image or file to derive important information. |
| [`CaptureMultiPages`](#capturemultipages) | Processes an image or file containing multiple pages to derive important information. |

## Capture

Process an image or file to derive important information. It can optionally use a specified template for the capture.

```cpp
CCapturedResult* Capture(const char* filePath, const char* templateName="");
CCapturedResult* Capture(const unsigned char *fileBytes, int fileSize, const char* templateName="");
CCapturedResult* Capture(const CImageData* pImageData, const char* templateName="");
```

**Parameters**

`[in] filePath` Specifies the path of the file to process.

`[in] templateName` Specifies a `CaptureVisionTemplate` to use for capturing.

`[in] fileBytes` Specifies the memory location containing the image to be processed.

`[in] fileSize`  Specifies the size of the image in bytes.

`[in] pImageData` Specifies the image data to process.

**Remarks**

- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_cpp_api }}capture-vision-router/auxiliary-classes/preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [InitSettings]({{ site.dcvb_cpp_api }}capture-vision-router/settings.html#initsettings) / [InitSettingsFromFile]({{ site.dcvb_cpp_api }}capture-vision-router/settings.html#initsettingsfromfile).
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `InitSettings` / `InitSettingsFromFile` and pass his own settings.
- If parameter `templateName` is not specified, the preset one named 'Default' will be used. However, if the preset ones have been overwritten as described above, the first `CaptureVisionTemplate` from the user's own settings will be used instead.

**Return Value**

Returns a pointer to a `CCapturedResult` object containing the captured items.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |
| EC_FILE_NOT_FOUND | -10005 | The file is not found. |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_MULTI_PAGES_NOT_SUPPORTED | -10066 | The api does not support multi-page files. Please use FileFetcher instead. |

**Code Snippet**

```cpp
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
if (errorCode != ErrorCode::EC_OK && errorCode != ErrorCode::EC_LICENSE_CACHE_USED)
{
    cout << "License initialization failed: ErrorCode: " << errorCode << ", ErrorString: " << szErrorMsg << endl;
}
else
{
    CCaptureVisionRouter* router = new CCaptureVisionRouter();
    CCapturedResult* result = router->Capture("path/to/file.png", "myTemplate");
    // other codes...
    result->Release();
    delete router;
}
```

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)
[CCapturedResult]({{ site.dcvb_cpp_api }}capture-vision-router/auxiliary-classes/captured-result.html)

## CaptureMultiPages

Processes an image or file containing multiple pages to derive important information.

```cpp
CCapturedResultArray* CaptureMultiPages(const char* filePath, const char* templateName="");
CCapturedResultArray* CaptureMultiPages(const unsigned char *fileBytes, int fileSize, const char* templateName="");
```

**Parameters**

`[in] filePath` Specifies the path of the file to process.

`[in] templateName` Specifies a `CaptureVisionTemplate` to use for capturing.

`[in] fileBytes` Specifies the memory location containing the image to be processed.

`[in] fileSize`  Specifies the size of the image in bytes.

**Remarks**

- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_cpp_api }}capture-vision-router/auxiliary-classes/preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [InitSettings]({{ site.dcvb_cpp_api }}capture-vision-router/settings.html#initsettings) / [InitSettingsFromFile]({{ site.dcvb_cpp_api }}capture-vision-router/settings.html#initsettingsfromfile).
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `InitSettings` / `InitSettingsFromFile` and pass his own settings.
- If parameter `templateName` is not specified, the preset one named 'Default' will be used. However, if the preset ones have been overwritten as described above, the first `CaptureVisionTemplate` from the user's own settings will be used instead.

**Return Value**

Returns a pointer to a `CCapturedResult` object containing the captured items.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |
| EC_FILE_NOT_FOUND | -10005 | The file is not found. |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |

**Code Snippet**

```cpp
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
if (errorCode != ErrorCode::EC_OK && errorCode != ErrorCode::EC_LICENSE_CACHE_USED)
{
    cout << "License initialization failed: ErrorCode: " << errorCode << ", ErrorString: " << szErrorMsg << endl;
}
else
{
    CCaptureVisionRouter* router = new CCaptureVisionRouter();
    CCapturedResultArray* resultArray = router->CaptureMultiPages("path/to/file.pdf", "myTemplate");
    for (int i = 0; i < resultArray->GetResultsCount(); i++)
    {
        const CCapturedResult* result = resultArray->GetResult(i);
        // other codes...
    }
    resultArray->Release();
    delete router;
}
```

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)
[CCapturedResultArray]({{ site.dcvb_cpp_api }}capture-vision-router/auxiliary-classes/captured-result-array.html)
[CCapturedResult]({{ site.dcvb_cpp_api }}capture-vision-router/auxiliary-classes/captured-result.html)