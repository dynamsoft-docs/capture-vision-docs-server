---
layout: default-layout
title: CaptureVisionRouter Auxiliary Methods - Dynamsoft Capture Vision Java Edition API
description: This page introduces auxiliary methods of the CaptureVisionRouter class of the Dynamsoft Capture Vision Java Edition.
keywords: capture vision, auxiliary, instance, api reference, Java
needAutoGenerateSidebar: true
needGenerateH3Content: false
---

# Auxiliary Methods - CaptureVisionRouter Class

| Method                                                      | Description                                               |
| ----------------------------------------------------------- | --------------------------------------------------------- |
| [`setGlobalIntraOpNumThreads`](#setglobalintraopnumthreads) | Sets the global number of threads used internally for model execution. |
| [`appendDLModelBuffer`](#appenddlmodelbuffer) | Appends a deep learning model to the memory buffer. |
| [`clearDLModelBuffers`](#cleardlmodelbuffers) | Clears all deep learning models from buffer to free up memory. |
| [`appendModelBuffer`](#appendmodelbuffer) | Deprecated. Will be removed in future versions. Use `appendDLModelBuffer` instead. |


## setGlobalIntraOpNumThreads

Sets the global number of threads used internally for model execution.

```java
public static void setGlobalIntraOpNumThreads(int size)
```

**Parameters**

`[in] size` Number of threads used internally for model execution. Valid range: [0, 256]. 
If the value is outside the range [0, 256], it will be treated as 0 (default).

**Remarks**

- Introduced in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.

## appendDLModelBuffer

Appends a deep learning model to the memory buffer.

```java
public static void appendDLModelBuffer(String modelName, byte[] modelBytes, int maxModelInstances) throws CaptureVisionException
```

**Parameters**

`[in] modelName` The name of the model.

`[in] modelBytes` The bytes of the model.

`[in] maxModelInstances` The max instances created for the model.

**Exceptions**

A [`CaptureVisionException`]({{ site.dcvb_java_api }}capture-vision-router/capture-vision-exception.html) is thrown when:

- The model buffer is invalid.
- Failed to allocate memory for the model.

**Remarks**

- Introduced in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.

## clearDLModelBuffers

Clears all deep learning models from buffer to free up memory.

```java
public static void clearDLModelBuffers()
```

**Remarks**

- After calling this function, all `CaptureVisionRouter` instances created before the function call will not be able to use model-related features.

- Introduced in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.

## appendModelBuffer

Deprecated. Will be removed in future versions. Use `appendDLModelBuffer` instead.

**Remarks**

- Deprecated in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.
