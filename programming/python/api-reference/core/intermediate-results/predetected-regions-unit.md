---
layout: default-layout
title: class PredetectedRegionsUnit - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class PredetectedRegionsUnit in Dynamsoft Core Module.
keywords: predetected regions, python
needAutoGenerateSidebar: true
---

# PredetectedRegionsUnit

The `PredetectedRegionsUnit` class represents a unit that contains a collection of pre-detected regions. It inherits from the `IntermediateResultUnit` class and stores the result of image color pre-detection.

## Definition

*Module:* dynamsoft_core

```python
class PredetectedRegionsUnit(IntermediateResultUnit)
```

## Methods

| Method | Description |
|--------|-------------|
| [`get_count`](#get_count) | Gets the number of pre-detected regions in the collection. |
| [`get_predetected_region`](#get_predetected_region) | Gets a specific pre-detected region in the collection. |
| [`remove_all_predetected_regions`](#remove_all_predetected_regions) | Removes all pre-detected regions in the unit. |
| [`remove_predetected_region`](#remove_predetected_region) | Removes a pre-detected region in the unit at the specified index. |
| [`add_predetected_region`](#add_predetected_region) | Adds a pre-detected region in the unit. |
| [`set_predetected_region`](#set_predetected_region) | Sets a pre-detected region in the unit at the specified index. |

### get_count

Gets the number of pre-detected regions in the collection.

```python
def get_count(self) -> int:
```

**Return value**

Returns the number of pre-detected regions in the collection.

### get_predetected_region

Gets a specific pre-detected region in the collection.

```python
def get_predetected_region(self, index: int) -> PredetectedRegionElement:
```

**Parameters**

`index` The index of the pre-detected region to retrieve.

**Return value**

Returns the specified pre-detected region in the collection.

**See Also**

[PredetectedRegionElement]({{ site.dcvb_python_api }}core/intermediate-results/predetected-region-element.html)

### remove_all_predetected_regions

Removes all pre-detected regions in the unit.

```python
def remove_all_predetected_regions(self) -> None:
```

### remove_predetected_region

Removes a pre-detected region in the unit at the specified index.

```python
def remove_predetected_region(self, index: int) -> int:
```

**Parameters**

`index` The index of the pre-detected region to remove.

**Return Value**

Returns 0 if succeeds, nonzero otherwise.

### add_predetected_region

Adds a pre-detected region in the unit.

```python
def add_predetected_region(self, element: PredetectedRegionElement, matrix_to_original_image: List[float] = IDENTITY_MATRIX):
```

**Parameters**

`element` The pre-detected region to add.
`matrix_to_original_image` The transform matrix to the original image.

**Return Value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[PredetectedRegionElement]({{ site.dcvb_python_api }}core/intermediate-results/predetected-region-element.html)

### set_predetected_region

Sets a pre-detected region in the unit at the specified index.

```python
def set_predetected_region(self, index: int, element: PredetectedRegionElement, matrix_to_original_image: List[float] = IDENTITY_MATRIX):
```

**Parameters** 

`index` The index of the pre-detected region to set.
`element` The pre-detected region to set.
`matrix_to_original_image` The transform matrix to the original image.

**Return Value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[PredetectedRegionElement]({{ site.dcvb_python_api }}core/intermediate-results/predetected-region-element.html)
