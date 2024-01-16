---
layout: default-layout
title: class CTextZone- Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CTextZone in Dynamsoft Core Module.
keywords: text zones, c++
needAutoGenerateSidebar: true
---

# CTextZone

The `CTextZone` class represents a single text zone.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore

```cpp
class CTextZone
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

```cpp
CTextZone();
CTextZone(const CQuadrilateral& loc);
CTextZone(const CQuadrilateral& loc, const int charContoursIndices[], int charContoursCount);
```

**Parameters**

`[in] loc` The location of the text zone.

`[in] charContoursIndices` The indices of the character contours.

`[in] charContoursCount` The count of the character contours.

### GetLocation

Gets the location of the text zone.

```cpp
CQuadrilateral GetLocation() const;
```

**Return Value**

Returns the location of the text zone.

### SetLocation

Sets the location of the text zone.

**Parameters**

`[in] loc` The location of the text zone.

```cpp
void SetLocation(const CQuadrilateral& loc);
```

### GetCharContoursIndices

Gets the indices of the character contours.

```cpp
void GetCharContoursIndices(int** ppCharContoursIndices, int* pCharContoursCount) const;
```

**Parameters**

`[in] ppCharContoursIndices` The indices of the character contours.

`[in] pCharContoursCount` The count of the character contours.

### SetCharContoursIndices

Sets the indices of the character contours.

**Parameters**

`[in] charContoursIndices` The indices of the character contours.

`[in] charContoursCount` The count of the character contours.

```cpp
void SetCharContoursIndices(const int charContoursIndices[], int charContoursCount);
```
