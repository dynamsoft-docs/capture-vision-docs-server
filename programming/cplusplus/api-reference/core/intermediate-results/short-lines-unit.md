---
layout: default-layout
title: class CShortLinesUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CShortLinesUnit in Dynamsoft Core Module.
keywords: Short lines, c++
needAutoGenerateSidebar: true
---

# CShortLinesUnit

The `CShortLinesUnit` class represents an intermediate result unit that contains the short lines. It is derived from the `CIntermediateResultUnit` class.

## Definition

*Namespace:dynamsoft::intermediate_results

*Assembly:DynamsoftCore

```cpp
class CShortLinesUnit : public CIntermediateResultUnit
```

## Methods Summary

| Method | Description |
| ------ | ----------- |
| [`GetCount`](#getcount) | Gets the number of short lines in the collection. |
| [`GetShortLine`](#getshortline) | Gets the short line at the specified index. |
| [`operator[]`](#operator) | Gets the short line at the specified index. |
| [`RemoveAllShortLines`](#removeallshortlines) | Removes all short lines from the unit. |
| [`RemoveShortLine`](#removeshortline) | Removes the short line at the specified index. |
| [`AddShortLine`](#addshortline) | Adds a short line to the unit. |
| [`SetShortLine`](#setshortline) | Sets the short line at the specified index. |

### GetCount

Gets the number of short lines in the collection.

```cpp
virtual int GetCount() const = 0;
```

**Return Value**Returns the number of short lines in the collection.

### GetShortLine

Gets the short line at the specified index.

```cpp
virtual const CLineSegmentGetShortLine(int index) const = 0;
```

**Parameters**

`index` The index of the short line to get.

**Return Value**

A pointer to the `CLineSegment` object that represents the short line at the specified index.

### operator[]

Gets the short line at the specified index.

```cpp
virtual const CLineSegmentoperator[](int index) const = 0;
```

**Parameters**

`index` The index of the short line to get.

**Return Value**

A pointer to the CLineSegment object that represents the short line at the specified index.

### RemoveAllShortLines

Removes all short lines from the unit.

```cpp
virtual void RemoveAllShortLines() = 0;
```

### RemoveShortLine

Removes the short line at the specified index.

```cpp
virtual int RemoveShortLine(int index) = 0;
```

**Parameters**

`index` The index of the short line to remove.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

### AddShortLine

Adds a short line to the unit.

```cpp
virtual int AddShortLine(const CLineSegment& line, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters**

`line` The short line to add.

`matrixToOriginalImage` The matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

### SetShortLine

Sets the short line at the specified index.

```cpp
virtual int SetShortLine(int index, const CLineSegment& line, const double matrixToOriginalImage[9] =  IDENTITY_MATRIX) = 0;
```

**Parameters**

`index` The index of the short line to set.

`line` The short line to set.

`matrixToOriginalImage` The matrix to original image.

**Return Value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.
