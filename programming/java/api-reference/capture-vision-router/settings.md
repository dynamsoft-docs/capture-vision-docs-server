---
layout: default-layout
title: CaptureVisionRouter Settings - Dynamsoft Capture Vision Router Module Java Edition API Reference
description: Definition of CaptureVisionRouter class Setting Methods in Dynamsoft Capture Vision Router Module Java Edition.
keywords: capture vision, router, settings, api reference, java
needAutoGenerateSidebar: true
needGenerateH3Content: false
---

# Setting Methods - CaptureVisionRouter Class

| Method                                            | Description                                                                                  |
| ------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| [`initSettings`](#initsettings)                   | Loads and initializes a template from a string.                                              |
| [`initSettingsFromFile`](#initsettingsfromfile)   | Loads and initializes a template from a file.                                                |
| [`outputSettings`](#outputsettings)               | Exports a specific `CaptureVisionTemplate` to a string.                                      |
| [`outputSettingsToFile`](#outputsettingstofile)   | Exports a specific `CaptureVisionTemplate` to a file.                                        |
| [`getSimplifiedSettings`](#getsimplifiedsettings) | Retrieves a `SimplifiedCaptureVisionSettings` object for a specific `CaptureVisionTemplate`. |
| [`updateSettings`](#updatesettings)               | Updates a `CaptureVisionTemplate` with `SimplifiedCaptureVisionSettings` object.             |
| [`resetSettings`](#resetsettings)                 | Resets all templates to factory settings.                                                    |
| [`getParameterTemplateCount`](#getparametertemplatecount)  | Gets the total number of available parameter templates.                                 |
| [`getParameterTemplateName`](#getparametertemplatename)    | Gets the name of a specific parameter template by its index.                            |

## initSettings

Loads and initializes a template from a string.

```java
public CaptureVisionError initSettings(String content) throws CaptureVisionException
```

**Parameters**

`content` The string containing the template.

**Return Value**

Returns a `CaptureVisionError` object that contains error information.

**Exceptions**

[`CaptureVisionException`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-exception.html)

**See Also**

[CaptureVisionError]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-error.html)

## initSettingsFromFile

Loads and initializes a template from a file.

```java
public CaptureVisionError initSettingsFromFile(String filePath) throws CaptureVisionException
```

**Parameters**

`filePath` The path to the file containing the template.

**Return Value**

Returns a `CaptureVisionError` object that contains error information.

**Exceptions**

[`CaptureVisionException`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-exception.html)

**See Also**

[CaptureVisionError]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-error.html)

## outputSettings

Exports a specific template to a string.

```java
public String outputSettings(String templateName) throws CaptureVisionException
public String outputSettings(String templateName, boolean includeDefaultValues) throws CaptureVisionException
```

**Parameters**

`templateName` The name of the `CaptureVisionTemplate` to be exported.

`includeDefaultValues` Specifies whether to include default values in the exported template.

**Remarks**

- It is supported to export all loaded templates by specifying the `templateName` as '*'.
- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_java_api }}capture-vision-router/enum-preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [initSettings]({{ site.dcvb_java_api }}capture-vision-router/settings.html#initsettings) / [initSettingsFromFile]({{ site.dcvb_java_api }}capture-vision-router/settings.html#initsettingsfromfile).
- When using a custom template, the parameter `templateName` should be the name of the [`CaptureVisionTemplate` object]({{ site.dcvb_parameters }}file/capture-vision-template.html) in the JSON template file.
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `initSettings` / `initSettingsFromFile` and pass his own settings.
- If parameter `templateName` is not specified, the preset one named 'Default' will be used. However, if the preset ones have been overwritten as described above, the first `CaptureVisionTemplate` from the user's own settings will be used instead.

**Return Value**

Returns a string containing the exported template.

**Exceptions**

[`CaptureVisionException`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-exception.html)

## outputSettingsToFile

Exports a specific template to a file.

```java
public void outputSettingsToFile(String templateName, String filePath) throws CaptureVisionException
public void outputSettingsToFile(String templateName, String filePath, boolean includeDefaultValues) throws CaptureVisionException
```

**Parameters**

`templateName` The name of the template to be exported.

`filePath` The path to the output file.

`includeDefaultValues` Specifies whether to include default values in the exported template.

**Remarks**

- It is supported to export all loaded templates by specifying the `templateName` as '*'.
- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_java_api }}capture-vision-router/enum-preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [initSettings]({{ site.dcvb_java_api }}capture-vision-router/settings.html#initsettings) / [initSettingsFromFile]({{ site.dcvb_java_api }}capture-vision-router/settings.html#initsettingsfromfile).
- When using a custom template, the parameter `templateName` should be the name of the [`CaptureVisionTemplate` object]({{ site.dcvb_parameters }}file/capture-vision-template.html) in the JSON template file.
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `initSettings` / `initSettingsFromFile` and pass his own settings.
- If parameter `templateName` is not specified, the preset one named 'Default' will be used. However, if the preset ones have been overwritten as described above, the first `CaptureVisionTemplate` from the user's own settings will be used instead.

**Exceptions**

[`CaptureVisionException`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-exception.html)

## getSimplifiedSettings

Retrieves a simplified version of the capture settings for a specific template.

```java
public SimplifiedCaptureVisionSettings getSimplifiedSettings(String templateName) throws CaptureVisionException
```

**Parameters**

`templateName` The name of the template.

**Remarks**

- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_java_api }}capture-vision-router/enum-preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [initSettings]({{ site.dcvb_java_api }}capture-vision-router/settings.html#initsettings) / [initSettingsFromFile]({{ site.dcvb_java_api }}capture-vision-router/settings.html#initsettingsfromfile).
- When using a custom template, the parameter `templateName` should be the name of the [`CaptureVisionTemplate` object]({{ site.dcvb_parameters }}file/capture-vision-template.html) in the JSON template file.
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `initSettings` / `initSettingsFromFile` and pass his own settings.
- If parameter `templateName` is not specified, the preset one named 'Default' will be used. However, if the preset ones have been overwritten as described above, the first `CaptureVisionTemplate` from the user's own settings will be used instead.

**Return Value**

Returns a `SimplifiedCaptureVisionSettings` object containing all settings.

**Exceptions**

[`CaptureVisionException`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-exception.html)

**See Also**

[SimplifiedCaptureVisionSettings]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html)

## updateSettings

Updates a template with simplified capture settings.

```java
public void updateSettings(String templateName, SimplifiedCaptureVisionSettings settings) throws CaptureVisionException
```

**Parameters**

`templateName` The name of the template to be updated.

`settings` A `SimplifiedCaptureVisionSettings` object.

**Remarks**

- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_java_api }}capture-vision-router/enum-preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [initSettings]({{ site.dcvb_java_api }}capture-vision-router/settings.html#initsettings) / [initSettingsFromFile]({{ site.dcvb_java_api }}capture-vision-router/settings.html#initsettingsfromfile).
- When using a custom template, the parameter `templateName` should be the name of the [`CaptureVisionTemplate` object]({{ site.dcvb_parameters }}file/capture-vision-template.html) in the JSON template file.
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `initSettings` / `initSettingsFromFile` and pass his own settings.
- If parameter `templateName` is not specified, the preset one named 'Default' will be used. However, if the preset ones have been overwritten as described above, the first `CaptureVisionTemplate` from the user's own settings will be used instead.

**Exceptions**

[`CaptureVisionException`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-exception.html)

**See Also**

[SimplifiedCaptureVisionSettings]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html)

## resetSettings

Resets all templates to factory settings.

```java
public void resetSettings() throws CaptureVisionException
```

**Exceptions**

[`CaptureVisionException`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-exception.html)

## getParameterTemplateCount

Gets the total number of available parameter templates.

```java
public int getParameterTemplateCount()
```

**Return value**

Returns an integer representing the count of parameter templates.

## getParameterTemplateName

Gets the name of a specific parameter template by its index.

```java
public String getParameterTemplateName(int index)
```

**Parameters**

`index` The index of the parameter template to get.

**Return value**

Returns a string containing the name of the parameter template.

