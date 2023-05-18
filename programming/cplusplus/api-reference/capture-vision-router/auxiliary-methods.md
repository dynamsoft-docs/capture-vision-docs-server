---
layout: default-layout
title: CaptureVisionRouter Auxiliary Methods - Dynamsoft Capture Vision C++ Edition API
description: This page introduces auxiliary methods of the CCaptureVisionRouter class of the Dynamsoft Capture Vision C++ Edition.
keywords: capture vision, auxiliary, instance, api reference, C++
needAutoGenerateSidebar: true
needGenerateH3Content: false
breadcrumbText: CVR C++ Auxiliary Methods
permalink: /programming/cplusplus/api-reference/capture-vision-router/auxiliary-methods.html
---

# Auxiliary Methods - Capture Vision Router C++ API Reference

| API Name                                                      | Description                                               |
| ------------------------------------------------------------- | --------------------------------------------------------- |
| [GetVersion](#getversion)                                     | Returns the version of the `CCaptureVisionRouter` object. |
| [FreeString](#freestring)                                     | Frees the memory allocated for a string.                  |

## GetVersion

Returns the version of the `CCaptureVisionRouter` object.

```cpp
static const char* GetVersion();
```

**Parameters**

None.

**Return Value**

Returns a const char pointer representing the version of the application.

## FreeString

Frees the memory allocated for a string.

```cpp
static void FreeString (char* content);
```

**Parameters**

`[in] content` The string whose memory needs to be freed.

**Return Value**

This function does not return a value. It simply frees the memory allocated for the input string.