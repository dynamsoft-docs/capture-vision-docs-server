---
layout: default-layout
title: CaptureVisionRouter Auxiliary Processing Methods - Dynamsoft Capture Vision Router Module .NET Edition API Reference
description: Definition of CaptureVisionRouter class Auxiliary Methods in Dynamsoft Capture Vision Router Module .NET Edition.
keywords: capture vision, auxiliary methods, api reference, .NET
needAutoGenerateSidebar: true
needGenerateH3Content: false
---

# Auxiliary Methods - CaptureVisionRouter Class

| Method                                                      | Description                                               |
| ----------------------------------------------------------- | --------------------------------------------------------- |
| [`SetGlobalIntraOpNumThreads`](#setglobalintraopnumthreads) | Sets the global number of threads used internally for model execution. |
| [`AppendDLModelBuffer`](#appenddlmodelbuffer) | Appends a deep learning model to the memory buffer. |
| [`ClearDLModelBuffers`](#cleardlmodelbuffers) | Clears all deep learning models from buffer to free up memory. |
| [`GetBufferedItemsManager`](#getbuffereditemsmanager) | Gets the manager instance of buffered items. |
| [`GetIntermediateResultManager`](#getintermediateresultmanager) | Returns an `IntermediateResultManager` object. |
| [`AppendModelBuffer`](#appendmodelbuffer) | Deprecated. Will be removed in future versions. Use `AppendDLModelBuffer` instead. |

## SetGlobalIntraOpNumThreads

Sets the global number of threads used internally for model execution.

```csharp
public static void SetGlobalIntraOpNumThreads(int intraOpNumThreads = 0)
```

**Parameters**

`[in] intraOpNumThreads` Number of threads used internally for model execution. Valid range: [0, 256]. 
If the value is outside the range [0, 256], it will be treated as 0 (default).

**Remarks**

- Introduced in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.

## AppendDLModelBuffer

Appends a deep learning model to the memory buffer.

```csharp
public static int AppendDLModelBuffer(string modelName, byte[] modelBytes, int maxModelInstances)
```

**Parameters**

`[in] modelName` The name of the model.

`[in] modelBytes` The bytes of the model.

`[in] maxModelInstances` The max instances created for the model.

**Return Value**

Returns 0 if succeeds, nonzero otherwise.

**Remarks**

- Introduced in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.

## ClearDLModelBuffers

Clears all deep learning models from buffer to free up memory.

```csharp
public static void ClearDLModelBuffers()
```

**Remarks**

- After calling this function, all `CaptureVisionRouter` instances created before the function call will not be able to use model-related features.

- Introduced in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.

## GetBufferedItemsManager

Gets the manager instance of buffered items.

```csharp
BufferedItemsManager GetBufferedItemsManager()
```

**Return Value**

Returns the [`BufferedItemsManager`](auxiliary-classes/buffered-items-manager.md) object.

**Remarks**

When the maximum number of buffered items is set to greater than 0, item buffering is enabled. Currently only character items can be buffered.

## GetIntermediateResultManager

Returns an [`IntermediateResultManager`](auxiliary-classes/intermediate-result-manager.md) object.

```csharp
IntermediateResultManager GetIntermediateResultManager()
```

**Parameters**

None.

**Return Value**

Returns the [`IntermediateResultManager`](auxiliary-classes/intermediate-result-manager.md) object.

## AppendModelBuffer

Deprecated. Will be removed in future versions. Use `AppendDLModelBuffer` instead.

**Remarks**

- Deprecated in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.
