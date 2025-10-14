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
| [`SetGlobalIntraOpNumThreads`](#setglobalintraopnumthreads) | Sets the global number of threads used internally for model execution. |
| [`AppendDLModelBuffer`](#appenddlmodelbuffer) | Appends a deep learning model to the memory buffer. |
| [`ClearDLModelBuffers`](#cleardlmodelbuffers) | Clears all deep learning models from buffer to free up memory. |
| [`FreeString`](#freestring) | Deprecated. Will be removed in future versions. Use [`CoreModule::FreeBytes`]({{ site.dcvb_cpp_api }}core/basic-structures/core-module.html#freebytes) instead.|
| [`AppendModelBuffer`](#appendmodelbuffer) | Deprecated. Will be removed in future versions. Use `AppendDLModelBuffer` instead. |


## SetGlobalIntraOpNumThreads

Sets the global number of threads used internally for model execution.

```cpp
static void SetGlobalIntraOpNumThreads(int intraOpNumThreads = 0);
```

**Parameters**

`[in] intraOpNumThreads` Number of threads used internally for model execution. Valid range: [0, 256]. 
If the value is outside the range [0, 256], it will be treated as 0 (default).

**Remarks**

- Introduced in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.

## AppendDLModelBuffer

Appends a deep learning model to the memory buffer.

```cpp
static int AppendDLModelBuffer(const char* modelName, const unsigned char* modelBytes, int modelBytesLength, int maxModelInstances);
```

**Parameters**

`[in] modelName` The name of the model.

`[in] modelBytes` The bytes of the model.

`[in] modelBytesLength` The length of the model bytes.

`[in] maxModelInstances` The max instances created for the model.

**Return Value**

Returns 0 if succeeds, nonzero otherwise.

**Remarks**

- Introduced in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.

## ClearDLModelBuffers

Clears all deep learning models from buffer to free up memory.

```cpp
static void ClearDLModelBuffers(); 
```

**Remarks**

- After calling this function, all `CaptureVisionRouter` instances created before the function call will not be able to use model-related features.

- Introduced in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.

## FreeString

Deprecated. Will be removed in future versions. Use [`CoreModule::FreeBytes`]({{ site.dcvb_cpp_api }}core/basic-structures/core-module.html#freebytes) instead.


## AppendModelBuffer

Deprecated. Will be removed in future versions. Use `AppendDLModelBuffer` instead.

**Remarks**

- Deprecated in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.
