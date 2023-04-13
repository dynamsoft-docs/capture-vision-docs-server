---
layout: default-layout
title: CaptureVisionRouter Auxiliary APIs - Dynamsoft Capture Vision C++ Edition API
description: This page introduces APIs related to the auxiliary APIs of CaptureVisionRouter of Dynamsoft Capture Vision C++ Edition.
keywords: capture vision, auxiliary, instance, api reference, C++, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
permalink: /programming/cplusplus/api-reference/cvr/auxiliary.html
---

# Capture Vision Router C++ API Reference - Auxiliary Methods

| API Name                                                      | Description                                               |
| ------------------------------------------------------------- | --------------------------------------------------------- |
| [GetIntermediateResultManager](#getintermediateresultmanager) | Returns an `CIntermediateResultManager` object.           |
| [GetVersion](#getversion)                                     | Returns the version of the `CCaptureVisionRouter` object. |
| [FreeString](#freestring)                                     | Frees the memory allocated for a string.                  |

## GetIntermediateResultManager

Returns an [`CIntermediateResultManager`](../core/intermediate-results/intermediate-result-manager.md) object.

```cpp
CIntermediateResultManager* GetIntermediateResultManager();
```

### Parameters

None.

### Return value

Returns a pointer to the [`CIntermediateResultManager`](../core/intermediate-results/intermediate-result-manager.md) object.

## GetVersion

Returns the version of the `CCaptureVisionRouter` object.

```cpp
static const char* GetVersion();
```

### Parameters

None.

### Return value

Returns a const char pointer representing the version of the application.

## FreeString

Frees the memory allocated for a string.

```cpp
static void FreeString (char* content);
```

### Parameters

`[in] content` The string whose memory needs to be freed.

### Return value

This function does not return a value. It simply frees the memory allocated for the input string.