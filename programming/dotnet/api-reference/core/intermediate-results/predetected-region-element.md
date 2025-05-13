---
layout: default-layout
title: class PredetectedRegionElement - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class PredetectedRegionElement in Dynamsoft Core Module.
keywords: predetected region element, .NET
needAutoGenerateSidebar: true
---

# PredetectedRegionElement

The `PredetectedRegionElement` class represents a region element that has been pre-detected in an image. It is a subclass of the `RegionObjectElement`.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results


```csharp
class PredetectedRegionElement : RegionObjectElement
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetModeName`](#getmodename)   | Gets the name of the detection mode used to detect this region element. |
| [`SetLocation`](#setlocation)   | Sets the location of the region object element. |
| [`GetLabelId`](#getlabelid)     | Gets the label id of the region object element. |
| [`GetLabelName`](#getlabelname) | Gets the label name of the region object element. |

### Inherited Methods

Checkout inherited methods from [RegionObjectElement]({{ site.dcvb_dotnet_api }}core/intermediate-results/region-object-element.html) for more details.

### GetModeName

Gets the name of the detection mode used to detect this region element.

```csharp
string GetModeName()
```

**Return value**

Returns the name of the detection mode used to detect this region element.

### SetLocation

Sets the location of the region object element.

```csharp
int SetLocation(Quadrilateral location)
```

**Parameters**

`location` The location of the region object element.

**Return value**

Returns 0 if success, otherwise an error code.

### GetLabelId

Gets the label id of the predetected region element.

```csharp
int GetLabelId()
```

**Return value**

Returns the label id of the predetected region element.

### GetLabelName

Gets the label name of the predetected region element.

```csharp
string GetLabelName()
```

**Return value**

Returns the label name of the predetected region element.