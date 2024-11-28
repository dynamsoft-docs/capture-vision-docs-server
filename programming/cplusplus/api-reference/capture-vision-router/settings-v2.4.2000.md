---
layout: default-layout
title: CaptureVisionRouter Settings - Dynamsoft Capture Vision C++ Edition API
description: This page introduces APIs related to the Settings of the CCaptureVisionRouter class of the Dynamsoft Capture Vision C++ Edition.
keywords: capture vision, router, settings, api reference, c++
needAutoGenerateSidebar: true
needGenerateH3Content: false
breadcrumbText: CVR C++ Settings
---

# Settings

| API Name                                          | Description                                                                                  |
| ------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| [`InitSettings`](#initsettings)                   | Loads and initializes a template from a string.                                              |
| [`InitSettingsFromFile`](#initsettingsfromfile)   | Loads and initializes a template from a file.                                                |
| [`OutputSettings`](#outputsettings)               | Exports a specific `CaptureVisionTemplate` to a string.                                      |
| [`OutputSettingsToFile`](#outputsettingstofile)   | Exports a specific `CaptureVisionTemplate` to a file.                                        |
| [`GetSimplifiedSettings`](#getsimplifiedsettings) | Retrieves a `SimplifiedCaptureVisionSettings` object for a specific `CaptureVisionTemplate`. |
| [`UpdateSettings`](#updatesettings)               | Updates a `CaptureVisionTemplate` with `SimplifiedCaptureVisionSettings` object.             |
| [`ResetSettings`](#resetsettings)                 | Resets all templates to factory settings.                                                    |

## InitSettings

Loads and initializes a template from a string.

```cpp
int InitSettings(const char* content, char errorMsgBuffer[]=NULL, const int errorMsgBufferLen=0)
```

**Parameters**

`[in] content` The string containing the template.

`[in] errorMsgBuffer` A buffer for error messages.

`[in] errorMsgBufferLen` The length of the error message buffer.

**Return value**

Returns an error code. Zero indicates success.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_JSON_PARSE_FAILED | -10030 | Failed to parse the JSON data. |
| EC_JSON_TYPE_INVALID | -10031 | One or more parameters are allocated with wrong data type. |
| EC_JSON_KEY_INVALID | -10032 | There exists invalid key in your JSON data. |
| EC_JSON_VALUE_INVALID | -10033 | There exists invalid parameter value in your JSON data. |
| EC_JSON_NAME_KEY_MISSING | -10034 | One or more `name` parameters are missing in your JSON data. Each section of the JSON data requires a unique `name` parameter. |
| EC_JSON_NAME_VALUE_DUPLICATED | -10035 | There exists duplicated `name` parameters in your JSON data. The `name` parameter should be unique. |
| EC_JSON_NAME_REFERENCE_INVALID | -10037 | You have referenced an invalid `name` value in your JSON data. |
| EC_PARAMETER_VALUE_INVALID | -10038 | There exists invalid parameter value in your JSON data. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

## InitSettingsFromFile

Loads and initializes a template from a file.

```cpp
int InitSettingsFromFile(const char* filePath, char errorMsgBuffer[]=NULL, const int errorMsgBufferLen=0)
```

**Parameters**

`[in] filePath` The path to the file containing the template.

`[in] errorMsgBuffer` A buffer for error messages.

`[in] errorMsgBufferLen` The length of the error message buffer.

**Return value**

Returns an error code. Zero indicates success.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_FILE_NOT_FOUND | -10005 | The file is not found. |
| EC_JSON_PARSE_FAILED | -10030 | Failed to parse the JSON data. |
| EC_JSON_TYPE_INVALID | -10031 | One or more parameters are allocated with wrong data type. |
| EC_JSON_KEY_INVALID | -10032 | There exists invalid key in your JSON data. |
| EC_JSON_VALUE_INVALID | -10033 | There exists invalid parameter value in your JSON data. |
| EC_JSON_NAME_KEY_MISSING | -10034 | One or more `name` parameters are missing in your JSON data. Each section of the JSON data requires a unique `name` parameter. |
| EC_JSON_NAME_VALUE_DUPLICATED | -10035 | There exists duplicated `name` parameters in your JSON data. The `name` parameter should be unique. |
| EC_JSON_NAME_REFERENCE_INVALID | -10037 | You have referenced an invalid `name` value in your JSON data. |
| EC_PARAMETER_VALUE_INVALID | -10038 | There exists invalid parameter value in your JSON data. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

## OutputSettings

Exports a specific template to a string.

```cpp
char* OutputSettings(const char* templateName, int* pErrorCode = NULL)
```

**Parameters**

`[in] templateName` The name of the template to export.

`[out] pErrorCode` An error code.

**Return value**

Returns a string containing the exported template. The string is allocated by the SDK and must be freed by calling [`FreeString`](auxiliary-methods.md#freestring).

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

**Remarks**

It is supported to export all loaded templates by specifying the `templateName` as '*'.

## OutputSettingsToFile

Exports a specific template to a file.

```cpp
int OutputSettingsToFile(const char* templateName, const char* filePath)
```

**Parameters**

`[in] templateName` The name of the template to export.

`[in] filePath` The path to the output file.

**Return value**

Returns an error code. Zero indicates success.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_FILE_SAVE_FAILED | -10058 | The file path is unavailable or the file can't be created for any other reasons. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

**Remarks**

It is supported to export all loaded templates by specifying the `templateName` as '*'.

## GetSimplifiedSettings

Retrieves a simplified version of the capture settings for a specific template.

```cpp
int GetSimplifiedSettings(const char* templateName, SimplifiedCaptureVisionSettings* settings)
```

**Parameters**

`[in] templateName` The name of the template.

`[out] settings` A pointer to a `SimplifiedCaptureVisionSettings` object.

**Return value**

Returns an error code. Zero indicates success.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CONVERT_COMPLEX_TEMPLATE_ERROR | -10061 | The template you specified is a complex template which can not be output as a `SimplifiedCaptureVisionSettings` object. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

**See Also**

[SimplifiedCaptureVisionSettings]({{ site.dcvb_cpp_api }}capture-vision-router/structs/simplified-capture-vision-settings.html)

## UpdateSettings

Updates a template with simplified capture settings.

```cpp
int UpdateSettings(const char* templateName, const SimplifiedCaptureVisionSettings* settings, char errorMsgBuffer[]=NULL, const int errorMsgBufferLen=0)
```

**Parameters**

`[in] templateName` The name of the template to update.

`[in] settings` A pointer to a `SimplifiedCaptureVisionSettings` object.

`[in] errorMsgBuffer` A buffer for error messages.

`[in] errorMsgBufferLen` The length of the error message buffer.

**Return value**

Returns an error code. Zero indicates success.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_PARAMETER_VALUE_INVALID | -10038 | There exists invalid parameter value in your `SimplifiedCaptureVisionSettings`. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

**See Also**

[SimplifiedCaptureVisionSettings]({{ site.dcvb_cpp_api }}capture-vision-router/structs/simplified-capture-vision-settings.html)

## ResetSettings

Resets all templates to factory settings.

```cpp
int ResetSettings()
```

**Return value**

Returns an error code. Zero indicates success.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
