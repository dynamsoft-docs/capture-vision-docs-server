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
| [`AppendModelBuffer`](#appendmodelbuffer)                       | Appends a model to the model buffer. |
| [`GetBufferedItemsManager`](#getbuffereditemsmanager)           | Gets the manager instance of buffered items.         |
| [`GetIntermediateResultManager`](#getintermediateresultmanager) | Returns an `IntermediateResultManager` object.           |

## AppendModelBuffer

Appends a model to the model buffer.

```csharp
public static int AppendModelBuffer(string modelName, byte[] modelBytes, int maxModelInstances)
```

**Parameters**

`[in] modelName` The name of the model.

`[in] modelBytes` The bytes of the model.

`[in] maxModelInstances` The max instances created for the model.

**Return Value**

Returns 0 if succeeds, nonzero otherwise.

## GetBufferedItemsManager

Gets the manager instance of buffered items.

```csharp
BufferedItemsManager GetBufferedItemsManager();
```

**Return Value**

Returns the [`BufferedItemsManager`](auxiliary-classes/buffered-items-manager.md) object.

**Remarks**

When the maximum number of buffered items is set to greater than 0, item buffering is enabled. Currently only character items can be buffered.

## GetIntermediateResultManager

Returns an [`IntermediateResultManager`](auxiliary-classes/intermediate-result-manager.md) object.

```csharp
IntermediateResultManager* GetIntermediateResultManager();
```

**Parameters**

None.

**Return Value**

Returns the [`IntermediateResultManager`](auxiliary-classes/intermediate-result-manager.md) object.
