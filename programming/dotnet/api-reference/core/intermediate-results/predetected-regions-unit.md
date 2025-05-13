---
layout: default-layout
title: class PredetectedRegionsUnit - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class PredetectedRegionsUnit in Dynamsoft Core Module.
keywords: predetected regions, .NET
needAutoGenerateSidebar: true
---

# PredetectedRegionsUnit

The `PredetectedRegionsUnit` class represents a unit that contains a collection of pre-detected regions. It inherits from the `IntermediateResultUnit` class and stores the result of image color pre-detection.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results


```csharp
class PredetectedRegionsUnit : IntermediateResultUnit, IEnumerable<PredetectedRegionElement>
```

## Methods Summary

| Method | Description |
|--------|-------------|
| [`GetCount`](#getcount) | Gets the number of pre-detected regions in the collection. |
| [`GetPredetectedRegion`](#getpredetectedregion) | Gets a specific pre-detected region in the collection. |
| [`GetPredetectedRegions`](#getpredetectedregions) | Gets all regions in the collection. |
| [`RemoveAllPredetectedRegions`](#removeallpredetectedregions) | Removes all pre-detected regions in the unit. |
| [`RemovePredetectedRegion`](#removepredetectedregion) | Removes a pre-detected region in the unit at the specified index. |
| [`AddPredetectedRegion`](#addpredetectedregion) | Adds a pre-detected region in the unit. |
| [`SetPredetectedRegion`](#setpredetectedregion) | Sets a pre-detected region in the unit at the specified index. |

### Inherited Methods

Checkout inherited methods from [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) for more details.

### GetCount

Gets the number of pre-detected regions in the collection.

```csharp
int GetCount()
```

**Return value**

Returns the number of pre-detected regions in the collection.

### GetPredetectedRegion

Gets a specific pre-detected region in the collection.

```csharp
PredetectedRegionElement GetPredetectedRegion(int index)
```

**Parameters**

`[in] index` The index of the pre-detected region to retrieve.

**Return value**

Returns the specified pre-detected region in the collection.

**See Also**

[PredetectedRegionElement]({{ site.dcvb_dotnet_api }}core/intermediate-results/predetected-region-element.html)

### GetPredetectedRegions

Gets all regions in the collection.

```csharp
PredetectedRegionElement[] GetPredetectedRegions()
```

**Return value**

Returns all the pre-detected regions.

**See Also**

[PredetectedRegionElement]({{ site.dcvb_dotnet_api }}core/intermediate-results/predetected-region-element.html)

### RemoveAllPredetectedRegions

Removes all pre-detected regions in the unit.

```csharp
void RemoveAllPredetectedRegions()
```

### RemovePredetectedRegion

Removes a pre-detected region in the unit at the specified index.

```csharp
int RemovePredetectedRegion(int index)
```

**Parameters**

`[in] index` The index of the pre-detected region to remove.

**Return Value**

Returns 0 if succeeds, nonzero otherwise.

### AddPredetectedRegion

Adds a pre-detected region in the unit.

```csharp
int AddPredetectedRegion(PredetectedRegionElement element, double[] matrixToOriginalImage = null)
```

**Parameters**

`[in] element` The pre-detected region to add.

`[in] matrixToOriginalImage` The matrix to original image.

**Return Value**

Returns 0 if succeeds, nonzero otherwise.

### SetPredetectedRegion

Sets a pre-detected region in the unit at the specified index.

```csharp
int SetPredetectedRegion(int index, PredetectedRegionElement element, double[] matrixToOriginalImage = null)
```

**Parameters** 

`[in] index` The index of the pre-detected region to set.

`[in] element` The pre-detected region to set.

`[in] matrixToOriginalImage` The matrix to original image.

**Return Value**

Returns 0 if succeeds, nonzero otherwise.
