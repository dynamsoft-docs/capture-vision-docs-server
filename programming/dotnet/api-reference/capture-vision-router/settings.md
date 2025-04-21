---
layout: default-layout
title: CaptureVisionRouter Settings - Dynamsoft Capture Vision Router Module .NET Edition API Reference
description: Definition of CaptureVisionRouter class Setting Methods in Dynamsoft Capture Vision Router Module .NET Edition.
keywords: capture vision, router, settings, api reference, .NET
needAutoGenerateSidebar: true
needGenerateH3Content: false
---

# Setting Methods - CaptureVisionRouter Class

| Method                                            | Description                                                                                  |
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

```csharp
int InitSettings(string content, out string errMsg)
```

**Parameters**

`[in] content` The string containing the template.

`[out] errMsg` Stores any error messages generated during the process.

**Return Value**

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

```csharp
int InitSettingsFromFile(string filePath, out string errMsg)
```

**Parameters**

`[in] filePath` The path to the file containing the template.

`[out] errMsg` Stores any error messages generated during the process.

**Return Value**

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

```csharp
string OutputSettings(string templateName, out int errorCode)
```

**Parameters**

`[in] templateName` The name of the `CaptureVisionTemplate` to export.

`[out] errorCode` An error code generated during the process.

**Remarks**

- It is supported to export all loaded templates by specifying the `templateName` as '*'.
- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [InitSettings]({{ site.dcvb_dotnet_api }}capture-vision-router/settings.html#initsettings) / [InitSettingsFromFile]({{ site.dcvb_dotnet_api }}capture-vision-router/settings.html#initsettingsfromfile).
- When using a custom template, the parameter `templateName` should be the name of the [`CaptureVisionTemplate` object]({{ site.dcvb_parameters }}file/capture-vision-template.html) in the JSON template file.
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `InitSettings` / `InitSettingsFromFile` and pass his own settings.

**Return Value**

Returns a string containing the exported template.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

## OutputSettingsToFile

Exports a specific template to a file.

```csharp
int OutputSettingsToFile(string templateName, string filePath)
```

**Parameters**

`[in] templateName` The name of the `CaptureVisionTemplate` to export.

`[in] filePath` The path to the output file.

**Remarks**

- It is supported to export all loaded templates by specifying the `templateName` as '*'.
- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [InitSettings]({{ site.dcvb_dotnet_api }}capture-vision-router/settings.html#initsettings) / [InitSettingsFromFile]({{ site.dcvb_dotnet_api }}capture-vision-router/settings.html#initsettingsfromfile).
- When using a custom template, the parameter `templateName` should be the name of the [`CaptureVisionTemplate` object]({{ site.dcvb_parameters }}file/capture-vision-template.html) in the JSON template file.
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `InitSettings` / `InitSettingsFromFile` and pass his own settings.

**Return Value**

Returns an error code. Zero indicates success.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_FILE_SAVE_FAILED | -10058 | The file path is unavailable or the file can't be created for any other reasons. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

## GetSimplifiedSettings

Retrieves a simplified version of the capture settings for a specific template.

```csharp
int GetSimplifiedSettings(string templateName, out SimplifiedCaptureVisionSettings settings)
```

**Parameters**

`[in] templateName` The name of the `CaptureVisionTemplate`.

`[out] settings` A `SimplifiedCaptureVisionSettings` object.

**Remarks**

- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [InitSettings]({{ site.dcvb_dotnet_api }}capture-vision-router/settings.html#initsettings) / [InitSettingsFromFile]({{ site.dcvb_dotnet_api }}capture-vision-router/settings.html#initsettingsfromfile).
- When using a custom template, the parameter `templateName` should be the name of the [`CaptureVisionTemplate` object]({{ site.dcvb_parameters }}file/capture-vision-template.html) in the JSON template file.
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `InitSettings` / `InitSettingsFromFile` and pass his own settings.

**Return Value**

Returns an error code. Zero indicates success.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CONVERT_COMPLEX_TEMPLATE_ERROR | -10061 | The template you specified is a complex template which can not be output as a `SimplifiedCaptureVisionSettings` object. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

**See Also**

[SimplifiedCaptureVisionSettings]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html)

## UpdateSettings

Updates a template with simplified capture settings.

```csharp
int UpdateSettings(string templateName, SimplifiedCaptureVisionSettings settings, out string errorMsg)
```

**Parameters**

`[in] templateName` The name of the `CaptureVisionTemplate` to update.

`[in] settings` A `SimplifiedCaptureVisionSettings` object.

`[out] errorMsg` Stores any error messages generated during the process.

**Remarks**

- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [InitSettings]({{ site.dcvb_dotnet_api }}capture-vision-router/settings.html#initsettings) / [InitSettingsFromFile]({{ site.dcvb_dotnet_api }}capture-vision-router/settings.html#initsettingsfromfile).
- When using a custom template, the parameter `templateName` should be the name of the [`CaptureVisionTemplate` object]({{ site.dcvb_parameters }}file/capture-vision-template.html) in the JSON template file.
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `InitSettings` / `InitSettingsFromFile` and pass his own settings.

**Return Value**

Returns an error code. Zero indicates success.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_PARAMETER_VALUE_INVALID | -10038 | There exists invalid parameter value in your `SimplifiedCaptureVisionSettings`. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

**See Also**

[SimplifiedCaptureVisionSettings]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html)

## ResetSettings

Resets all templates to factory settings.

```csharp
int ResetSettings()
```

**Return Value**

Returns an error code. Zero indicates success.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
