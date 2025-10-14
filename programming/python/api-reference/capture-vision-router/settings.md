---
layout: default-layout
title: CaptureVisionRouter Settings - Dynamsoft Capture Vision Router Module Python Edition API Reference
description: Definition of CaptureVisionRouter class Setting Methods in Dynamsoft Capture Vision Router Module Python Edition.
keywords: capture vision, router, settings, api reference, python
needAutoGenerateSidebar: true
needGenerateH3Content: false
---

# Setting Methods - CaptureVisionRouter Class

| Method                                            | Description                                                                                  |
| ------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| [`init_settings`](#init_settings)                   | Loads and initializes a template from a string.                                              |
| [`init_settings_from_file`](#init_settings_from_file)   | Loads and initializes a template from a file.                                                |
| [`output_settings`](#output_settings)               | Exports a specific `CaptureVisionTemplate` to a string.                                      |
| [`output_settings_to_file`](#output_settings_to_file)   | Exports a specific `CaptureVisionTemplate` to a file.                                        |
| [`get_simplified_settings`](#get_simplified_settings) | Retrieves a `SimplifiedCaptureVisionSettings` object for a specific `CaptureVisionTemplate`. |
| [`update_settings`](#update_settings)               | Updates a `CaptureVisionTemplate` with `SimplifiedCaptureVisionSettings` object.             |
| [`reset_settings`](#reset_settings)                 | Resets all templates to factory settings.                                                    |
| [`get_parameter_template_count`](#get_parameter_template_count)  | Gets the total number of available parameter templates.                                 |
| [`get_parameter_template_name`](#get_parameter_template_name)    | Gets the name of a specific parameter template by its index.                            |
| [`switch_capturing_template`](#switch_capturing_template)      | Switches the capturing template during the image processing workflow.                            |

## init_settings

Loads and initializes a template from a string.

```python
def init_settings(self, content: str) -> Tuple[int, str]:
```

**Parameters**

`content` The string containing the template.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html)

## init_settings_from_file

Loads and initializes a template from a file.

```python
def init_settings_from_file(self, file_path: str) -> Tuple[int, str]:
```

**Parameters**

`file_path` The path to the file containing the template.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html)

## output_settings

Exports a specific template to a string.

```python
def output_settings(self, template_name: str, include_default_values: bool = False) -> Tuple[int, str, str]:
```

**Parameters**

`template_name` The name of the `CaptureVisionTemplate` to be exported.

`include_default_values` Specifies whether to include default values in the exported template.

**Remarks**

- It is supported to export all loaded templates by specifying the `template_name` as '*'.
- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_python_api }}capture-vision-router/enum-preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [init_settings]({{ site.dcvb_python_api }}capture-vision-router/settings.html#init_settings) / [init_settings_from_file]({{ site.dcvb_python_api }}capture-vision-router/settings.html#init_settings_from_file).
- When using a custom template, the parameter `template_name` should be the name of the [`CaptureVisionTemplate` object]({{ site.dcvb_parameters }}file/capture-vision-template.html) in the JSON template file.
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `init_settings` / `init_settings_from_file` and pass his own settings.
- If parameter `template_name` is not specified, the preset one named 'Default' will be used. However, if the preset ones have been overwritten as described above, the first `CaptureVisionTemplate` from the user's own settings will be used instead.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.
- `template_content` <*str*>: A string containing the exported template.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html)

## output_settings_to_file

Exports a specific template to a file.

```python
def output_settings_to_file(self, template_name: str, file_path: str, include_default_values: bool = False) -> Tuple[int, str]:
```

**Parameters**

`template_name` The name of the template to be exported.

`file_path` The path to the output file.

`include_default_values` Specifies whether to include default values in the exported template.

**Remarks**

- It is supported to export all loaded templates by specifying the `template_name` as '*'.
- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_python_api }}capture-vision-router/enum-preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [init_settings]({{ site.dcvb_python_api }}capture-vision-router/settings.html#init_settings) / [init_settings_from_file]({{ site.dcvb_python_api }}capture-vision-router/settings.html#init_settings_from_file).
- When using a custom template, the parameter `template_name` should be the name of the [`CaptureVisionTemplate` object]({{ site.dcvb_parameters }}file/capture-vision-template.html) in the JSON template file.
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `init_settings` / `init_settings_from_file` and pass his own settings.
- If parameter `template_name` is not specified, the preset one named 'Default' will be used. However, if the preset ones have been overwritten as described above, the first `CaptureVisionTemplate` from the user's own settings will be used instead.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html)

## get_simplified_settings

Retrieves a simplified version of the capture settings for a specific template.

```python
def get_simplified_settings(self, template_name: str) -> Tuple[int, str, SimplifiedCaptureVisionSettings]:
```

**Parameters**

`template_name` The name of the template.

**Remarks**

- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_python_api }}capture-vision-router/enum-preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [init_settings]({{ site.dcvb_python_api }}capture-vision-router/settings.html#init_settings) / [init_settings_from_file]({{ site.dcvb_python_api }}capture-vision-router/settings.html#init_settings_from_file).
- When using a custom template, the parameter `template_name` should be the name of the [`CaptureVisionTemplate` object]({{ site.dcvb_parameters }}file/capture-vision-template.html) in the JSON template file.
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `init_settings` / `init_settings_from_file` and pass his own settings.
- If parameter `template_name` is not specified, the preset one named 'Default' will be used. However, if the preset ones have been overwritten as described above, the first `CaptureVisionTemplate` from the user's own settings will be used instead.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.
- `settings` <*SimplifiedCaptureVisionSettings*>: A `SimplifiedCaptureVisionSettings` object containing all settings.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html)

[SimplifiedCaptureVisionSettings]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html)

## update_settings

Updates a template with simplified capture settings.

```python
def update_settings(self, template_name: str, settings: SimplifiedCaptureVisionSettings) -> Tuple[int, str]:
```

**Parameters**

`template_name` The name of the template to be updated.

`settings` A `SimplifiedCaptureVisionSettings` object.

**Remarks**

- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_python_api }}capture-vision-router/enum-preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [init_settings]({{ site.dcvb_python_api }}capture-vision-router/settings.html#init_settings) / [init_settings_from_file]({{ site.dcvb_python_api }}capture-vision-router/settings.html#init_settings_from_file).
- When using a custom template, the parameter `template_name` should be the name of the [`CaptureVisionTemplate` object]({{ site.dcvb_parameters }}file/capture-vision-template.html) in the JSON template file.
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `init_settings` / `init_settings_from_file` and pass his own settings.
- If parameter `template_name` is not specified, the preset one named 'Default' will be used. However, if the preset ones have been overwritten as described above, the first `CaptureVisionTemplate` from the user's own settings will be used instead.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html)

[SimplifiedCaptureVisionSettings]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html)

## reset_settings

Resets all templates to factory settings.

```python
def reset_settings(self) -> Tuple[int, str]:
```

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html)

## get_parameter_template_count

Gets the total number of available parameter templates.

```python
def get_parameter_template_count(self) -> int:
```

**Return value**

Returns an integer representing the count of parameter templates.

## get_parameter_template_name

Gets the name of a specific parameter template by its index.

```python
def get_parameter_template_name(self, index: int) -> Tuple[int, str]:
```

**Parameters**

`index` The index of the parameter template to get.

**Return value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `template_name` <*str*>: The name of the parameter template.

## switch_capturing_template

Switches the capturing template during the image processing workflow.

```python
def switch_capturing_template(self, template_name: str) -> Tuple[int, str]:
```

**Parameters**

`template_name` The name of the new capturing template to apply.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**Remarks**

- Introduced in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html)
