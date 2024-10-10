---
layout: default-layout
title: class CImageSourceErrorListener - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the C++ edition of the class CImageSourceErrorListener in Core Module.
keywords: imagesource error listener, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# CImageSourceErrorListener

The `CImageSourceErrorListener` class is an abstract base class for receiving error notifications from an image source.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore

```cpp
class CImageSourceErrorListener 
```

## Methods Summary

| Method | Description |
| ------ | ----------- |
| [`OnErrorReceived`](#onerrorreceived) | Called when an error is received from the image source. |

### OnErrorReceived

Called when an error is received from the image source.

```cpp
virtual void OnErrorReceived(int errorCode, const char* errorMessage)
```

**Parameters**

`[in] errorCode` The integer error code indicating the type of error.

`[in] errorMessage` A C-style string containing the error message providing additional information about the error.

**See Also**

[ErrorCode]({{ site.dcvb_enumerations }}core/error-code.html?src=cpp&&lang=cpp)
