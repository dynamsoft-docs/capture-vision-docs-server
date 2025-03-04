---
layout: default-layout
title: CaptureVisionRouter Auxiliary Methods - Dynamsoft Capture Vision C++ Edition API
description: This page introduces auxiliary methods of the CCaptureVisionRouter class of the Dynamsoft Capture Vision C++ Edition.
keywords: capture vision, auxiliary, instance, api reference, C++
needAutoGenerateSidebar: true
needGenerateH3Content: false
breadcrumbText: CVR C++ Auxiliary Methods
---

# Auxiliary Methods - Capture Vision Router C++ API Reference

| API Name                                                      | Description                                               |
| ------------------------------------------------------------- | --------------------------------------------------------- |
| [`FreeString`](#freestring)                                     | Frees the memory allocated for a string.                  |
| [`AppendModelBuffer`](#appendmodelbuffer)                       | Appends a model to the model buffer. |

## FreeString

Frees the memory allocated for a string. The function is *deprecated*, use [`CoreModule::FreeBytes`]({{ site.dcvb_cpp_api }}core/basic-structures/core-module.html#freebytes) instead.

```cpp
static void FreeString(char* content);
```

**Parameters**

`[in] content` The string whose memory needs to be freed.

**Return Value**

This function does not return a value. It simply frees the memory allocated for the input string.

## AppendModelBuffer

Appends a model to the model buffer.

```cpp
static int AppendModelBuffer(const char* modelName, const unsigned char* modelBytes, int modelBytesLength, int maxModelInstances);
```

**Parameters**

`[in] modelName` The name of the model.

`[in] modelBytes` The bytes of the model.

`[in] modelBytesLength` The length of the model bytes.

`[in] maxModelInstances` The max instances created for the model.

**Return Value**

Returns 0 if succeeds, nonzero otherwise.
