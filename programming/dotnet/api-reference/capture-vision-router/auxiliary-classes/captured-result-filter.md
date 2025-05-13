---
layout: default-layout
title: CapturedResultFilter Class - Dynamsoft Capture Vision Module .NET Edition API Reference
description: Definition of CapturedResultFilter class in Dynamsoft Capture Vision Module .NET Edition.
keywords: captured result receiver, .NET
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# CapturedResultFilter

The `CapturedResultFilter` class is responsible for filtering captured results. It contains several callback functions for different types of results, including original image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.

>Note: Currently, user defined `CapturedResultFilter` is not supported.

## Definition

*Namespace:* Dynamsoft.CVR


```csharp
public class CapturedResultFilter : IDisposable 
```

## Methods

| Method                                                            | Description                                          |
| ----------------------------------------------------------------- | ---------------------------------------------------- |
| [`GetName`](#getname)       | Gets the name of the captured result filter.                                             |
| [`SetName`](#setname)       | Sets the name of the captured result filter.                                             |


### GetName

Gets the name of the captured result filter.  

```csharp
string GetName()
```

**Return Value**

Returns the name of the captured result filter.  

### SetName

Sets the name of the captured result filter.  

```csharp
void SetName(string name)
```

**Parameters**

`[in] name` The name of the captured result filter.
