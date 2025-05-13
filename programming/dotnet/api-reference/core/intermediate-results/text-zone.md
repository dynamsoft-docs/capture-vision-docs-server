---
layout: default-layout
title: class TextZone- Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class TextZone in Dynamsoft Core Module.
keywords: text zones, .NET
needAutoGenerateSidebar: true
---

# TextZone

The `TextZone` class represents a single text zone.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results


```csharp
class TextZone
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`Constructors`](#constructors) | The constructors. |
| [`GetLocation`](#getlocation) | Gets the location of the text zone. |
| [`SetLocation`](#setlocation) | Sets the location of the text zone. |
| [`GetCharContoursIndices`](#getcharcontoursindices) | Gets the indices of the character contours. |
| [`SetCharContoursIndices`](#setcharcontoursindices) | Sets the indices of the character contours. |

### Constructors

The constructors.

```csharp
TextZone();
TextZone(Quadrilateral location);
TextZone(Quadrilateral location, int[] charContoursIndices);
```

**Parameters**

`[in] location` The location of the text zone.

`[in] charContoursIndices` The indices of the character contours.

### GetLocation

Gets the location of the text zone.

```csharp
Quadrilateral GetLocation()
```

**Return Value**

Returns the location of the text zone.

**See Also**

[Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)

### SetLocation

Sets the location of the text zone.

```csharp
void SetLocation(Quadrilateral location)
```

**Parameters**

`[in] location` The location of the text zone.

**See Also**

[Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)

### GetCharContoursIndices

Gets the indices of the character contours.

```csharp
int[] GetCharContoursIndices()
```

### SetCharContoursIndices

Sets the indices of the character contours.

```csharp
void SetCharContoursIndices(int[] charContoursIndices)
```

**Parameters**

`[in] charContoursIndices` The indices of the character contours.
