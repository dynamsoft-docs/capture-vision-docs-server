---
layout: default-layout
title: class TextZonesUnit - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class TextZonesUnit in Dynamsoft Core Module.
keywords: text zones, .NET
needAutoGenerateSidebar: true
---

# TextZonesUnit

The `TextZonesUnit` class represents a unit that contains text zones. It is derived from `IntermediateResultUnit` class and provides methods to retrieve the count and details of text zones.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results


```csharp
class TextZonesUnit : IntermediateResultUnit
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetCount`](#getcount) | Gets the number of text zones.|
| [`GetTextZone`](#gettextzone) | Gets the quadrilateral shape of the text zone at the specified index. |
| [`GetTextZones`](#gettextzones) | Gets all the text zones. |
| [`RemoveAllTextZones`](#removealltextzones) | Removes all text zones from the unit. |
| [`RemoveTextZone`](#removetextzone) | Removes the text zone at the specified index. |
| [`AddTextZone`](#addtextzone) | Adds a text zone to the unit. |
| [`SetTextZone`](#settextzone) | Sets the text zone at the specified index. |

### Inherited Methods

Checkout inherited methods from [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) for more details.

### GetCount

Gets the number of text zones in the unit.

```csharp
int GetCount()
```

**Return value**

Returns the number of text zones in the unit.

### GetTextZone

Gets the quadrilateral shape of the text zone at the specified index.

```csharp
int GetTextZone(int index, out TextZone textZone)
```

**Parameters**

`[in] index` The index of the text zone.

`[in, out] textZone` The received text zone.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

**See Also**

[TextZone]({{ site.dcvb_dotnet_api }}core/basic-classes/text-zone.html)

### GetTextZones

Gets all the text zones.

```csharp
int GetTextZones(out TextZone[] textZones)
```

**Parameters**

`[in, out] textZone` All the received text zones.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

**See Also**

[TextZone]({{ site.dcvb_dotnet_api }}core/basic-classes/text-zone.html)

### RemoveAllTextZones

Removes all text zones from the unit.

```csharp
void RemoveAllTextZones()
```

### RemoveTextZone

Removes the text zone at the specified index.

```csharp
int RemoveTextZone(int index)
```

**Parameters**

`[in] index` The index of the text zone to remove.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

### AddTextZone

Adds a text zone to the unit.

```csharp
int AddTextZone(TextZone textZone, double[] matrixToOriginalImage = null)
```

**Parameters**

`[in] textZone` The text zone to add.

`[in] matrixToOriginalImage` The matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

**See Also**

[TextZone]({{ site.dcvb_dotnet_api }}core/basic-classes/text-zone.html)

### SetTextZone

Sets the text zone at the specified index.

```csharp
int SetTextZone(int index, TextZone textZone, double[] matrixToOriginalImage = null)
```

**Parameters**

`[in] index` The index of the text zone to set.

`[in] textZone` The text zone to set.

`[in] matrixToOriginalImage` The matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

**See Also**

[TextZone]({{ site.dcvb_dotnet_api }}core/basic-classes/text-zone.html)
