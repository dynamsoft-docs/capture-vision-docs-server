---
layout: default-layout
title: class AuxiliaryRegionElement - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class AuxiliaryRegionElement in Dynamsoft Core Module.
keywords: auxiliary region element, .NET
---

# AuxiliaryRegionElement

The `AuxiliaryRegionElement` class represents an auxiliary region element that contains additional region information detected during processing (e.g., MRZ, portrait zones, signature areas). It inherits from the `RegionObjectElement` class.

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results

*Inheritance:* [RegionObjectElement]({{ site.dcvb_dotnet_api }}core/intermediate-results/region-object-element.html) -> AuxiliaryRegionElement

```csharp
public class AuxiliaryRegionElement : RegionObjectElement
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`AuxiliaryRegionElement`](#auxiliaryregionelement) | Constructor. Initializes a new instance of the `AuxiliaryRegionElement` class. |
| [`GetName`](#getname) | Gets the name of this auxiliary region. |
| [`GetConfidence`](#getconfidence) | Gets the confidence level of this auxiliary region detection. |
| [`SetName`](#setname) | Sets the name of this auxiliary region. |
| [`SetLocation`](#setlocation) | Sets the location of this auxiliary region. |
| [`SetConfidence`](#setconfidence) | Sets the confidence level of this auxiliary region detection. |
| **Methods Inherited from [RegionObjectElement]({{ site.dcvb_dotnet_api }}core/intermediate-results/region-object-element.html):** | |
| [`GetLocation`]({{ site.dcvb_dotnet_api }}core/intermediate-results/region-object-element.html#getlocation) | Gets the location of the region object element. |
| [`GetReferencedElement`]({{ site.dcvb_dotnet_api }}core/intermediate-results/region-object-element.html#getreferencedelement) | Gets a referenced region object element. |
| [`GetElementType`]({{ site.dcvb_dotnet_api }}core/intermediate-results/region-object-element.html#getelementtype) | Gets the type of the region object element. |
| [`GetImageData`]({{ site.dcvb_dotnet_api }}core/intermediate-results/region-object-element.html#getimagedata) | Gets the imageData of the region object element. |
| [`Clone`]({{ site.dcvb_dotnet_api }}core/intermediate-results/region-object-element.html#clone) | Clones the region object element. |

### AuxiliaryRegionElement

Constructor. Initializes a new instance of the `AuxiliaryRegionElement` class.

```csharp
AuxiliaryRegionElement()
```

### GetName

Gets the name of this auxiliary region.

```csharp
string GetName()
```

**Return value**

Returns a string representing the region name (e.g., "MRZ", "PortraitZone", "SignatureArea").

### GetConfidence

Gets the confidence level of this auxiliary region detection.

```csharp
int GetConfidence()
```

**Return value**

Returns the confidence value, typically in the range [0, 100].

### SetName

Sets the name of this auxiliary region.

```csharp
void SetName(string name)
```

**Parameters**

`name` The region name to set (e.g., "MRZ", "PortraitZone", "SignatureArea").

### SetLocation

Sets the location of this auxiliary region.

```csharp
int SetLocation(Quadrilateral location)
```

**Parameters**

`location` A `Quadrilateral` object defining the region boundaries.

**Return value**

Returns 0 if successful, otherwise returns an error code.

**See Also**

[Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)

### SetConfidence

Sets the confidence level of this auxiliary region detection.

```csharp
void SetConfidence(int confidence)
```

**Parameters**

`confidence` The confidence value to set, typically in the range [0, 100].
