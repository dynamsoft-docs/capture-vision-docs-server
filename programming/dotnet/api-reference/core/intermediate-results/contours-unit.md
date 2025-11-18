---
layout: default-layout
title: class ContoursUnit - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class ContoursUnit in Dynamsoft Core Module.
keywords: contours, .NET
needAutoGenerateSidebar: true
---

# ContoursUnit

The `ContoursUnit` class represents a unit that contains contours as intermediate results. It is derived from the `IntermediateResultUnit` class.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results


```csharp
class ContoursUnit : IntermediateResultUnit
```

## Methods

| Method                    | Description |
|---------------------------|---------------------------------------------|
| [`GetContours`](#getcontours) | Gets the contours.  |
| [`SetContours`](#setcontours) | Sets the contours.  |

### Inherited Methods

Checkout inherited methods from [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) for more details.

### GetContours

Gets the contours.

```csharp
int GetContours(out Contour[] contours, out Vector4[] hierarchies)
```

**Parameters**

`[out] contours` The contours in the unit.

`[out] hierarchies` The hierarchies of the contours in the unit.

**Return value**

Returns 0 if successful, or an error code if the contour could not be retrieved.

**See Also**

[Contour]({{ site.dcvb_dotnet_api }}core/basic-classes/contour.html)

[Vector4]({{ site.dcvb_dotnet_api }}core/basic-classes/vector4.html)

### SetContours

Sets the contours and hierarchies in the unit.

```csharp
int SetContours(Contour[] contours, Vector4[] hierarchies, double[] matrixToOriginalImage = null)
```

**Parameters**

`[in] contours` The contours in the unit.

`[in] hierarchies` The hierarchies in the unit.

`[in] matrixToOriginalImage` The matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.
