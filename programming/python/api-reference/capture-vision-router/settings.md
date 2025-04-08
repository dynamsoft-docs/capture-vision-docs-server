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

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html?lang=python)

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

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html?lang=python)

## output_settings

Exports a specific template to a string.

```python
def output_settings(self, template_name: str, include_default_values: bool = False) -> Tuple[int, str, str]:
```

**Parameters**

`template_name` The name of the template to be exported.

`include_default_values` Specifies whether to include default values in the exported template.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.
- `template_content` <*str*>: A string containing the exported template.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html?lang=python)

**Remarks**

It is supported to export all loaded templates by specifying the `template_name` as '*'.

## output_settings_to_file

Exports a specific template to a file.

```python
def output_settings_to_file(self, template_name: str, file_path: str, include_default_values: bool = False) -> Tuple[int, str]:
```

**Parameters**

`template_name` The name of the template to be exported.

`file_path` The path to the output file.

`include_default_values` Specifies whether to include default values in the exported template.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html?lang=python)

**Remarks**

It is supported to export all loaded templates by specifying the `template_name` as '*'.

## get_simplified_settings

Retrieves a simplified version of the capture settings for a specific template.

```python
def get_simplified_settings(self, template_name: str) -> Tuple[int, str, SimplifiedCaptureVisionSettings]:
```

**Parameters**

`template_name` The name of the template.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.
- `settings` <*SimplifiedCaptureVisionSettings*>: A `SimplifiedCaptureVisionSettings` object containing all settings.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html?lang=python)

[SimplifiedCaptureVisionSettings]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html)

## update_settings

Updates a template with simplified capture settings.

```python
def update_settings(self, template_name: str, settings: SimplifiedCaptureVisionSettings) -> Tuple[int, str]:
```

**Parameters**

`template_name` The name of the template to be updated.

`settings` A `SimplifiedCaptureVisionSettings` object.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html?lang=python)

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

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html?lang=python)

