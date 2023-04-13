---
layout: default-layout
title: CaptureVisionRouter Settings - Dynamsoft Capture Vision C++ Edition API
description: This page introduces APIs related to the Settings of the CCaptureVisionRouter class of the Dynamsoft Capture Vision C++ Edition.
keywords: capture vision, router, settings, api reference, c++
needAutoGenerateSidebar: true
needGenerateH3Content: false
breadcrumbText: CVR C++ Settings
permalink: /programming/cplusplus/api-reference/capture-vision-router/settings.html
---

# Capture Vision Router C++ API Reference - Settings

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

## OutputSettings

Exports a specific template to a string.

```cpp
char* OutputSettings(const char* templateName, int* pErrorCode = NULL)
```

**Parameters**

`[in] templateName` The name of the template to export.

`[out] pErrorCode` An error code.

**Return value**

Returns a string containing the exported template. The string is allocated by the SDK and must be freed by calling `FreeString`.

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

## ResetSettings

Resets all templates to factory settings.

```cpp
void ResetSettings()
```