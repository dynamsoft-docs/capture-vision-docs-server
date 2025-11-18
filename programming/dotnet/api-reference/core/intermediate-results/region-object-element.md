---
layout: default-layout
title: class RegionObjectElement - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class RegionObjectElement in Dynamsoft Core Module.
keywords: region object element, .NET
needAutoGenerateSidebar: true
---

# RegionObjectElement

The `RegionObjectElement` class represents an element of a region object in 2D space. It is an abstract class that provides the interface for region object elements.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results


```csharp
class RegionObjectElement : IDisposable
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetLocation`](#getlocation) | Gets the location of the region object element. |
| [`GetReferencedElement`](#getreferencedelement) | Gets a referenced region object element. |
| [`GetElementType`](#getelementtype) | Gets the type of the region object element. |
| [`GetImageData`](#getimagedata) | Gets the imageData of the region object element. |
| [`Clone`](#clone) | Clone the region object element. |

### GetLocation

Gets the location of the region object element.

```csharp
Quadrilateral GetLocation()
```

**Return value**

Returns a `Quadrilateral` object which represents the location of the region object element.

**See Also**

[Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)

### GetReferencedElement

Gets a referenced region object element.

```csharp
RegionObjectElement GetReferencedElement()
```

**Return value**

Returns a referenced `RegionObjectElement` object.

**See Also**

[RegionObjectElement]({{ site.dcvb_dotnet_api }}core/intermediate-results/region-object-element.html)

### GetElementType

Gets the type of the region object element.

```csharp
EnumRegionObjectElementType GetElementType()
```

**Return value**

Returns a `EnumRegionObjectElementType` enum value which represents the type of the region object element.

**See Also**

[EnumRegionObjectElementType]({{ site.dcvb_dotnet_api }}core/enum-region-object-element-type.html)

### GetImageData

Gets the imageData of the region object element.

```csharp
ImageData GetImageData()
```

**Return value**

Returns a referenced `ImageData` object.

### Clone

Clone the region object element.

```csharp
RegionObjectElement Clone()
```

**Return value**

Returns a copy of the region object element.

