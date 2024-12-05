---
layout: default-layout
title: class RegionObjectElement - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class RegionObjectElement in Dynamsoft Core Module.
keywords: region object element, python
needAutoGenerateSidebar: true
---

# RegionObjectElement

The `RegionObjectElement` class represents an element of a region object in 2D space. It is an abstract class that provides the interface for region object elements.

## Definition

*Module:* dynamsoft_core

```python
class RegionObjectElement 
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_location`](#get_location) | Gets the location of the region object element. |
| [`get_referenced_element`](#get_referenced_element) | Gets a referenced region object element. |
| [`get_element_type`](#get_element_type) | Gets the type of the region object element. |
| [`set_location`](#set_location) | Sets the location of the region object element. |
| [`clone`](#clone) | Clones the region object element. |

### get_location

Gets the location of the region object element.

```python
def get_location(self) -> Quadrilateral:
```

**Return value**

Returns a `Quadrilateral` object which represents the location of the region object element.

**See Also**

[Quadrilateral]({{ site.dcvb_python_api }}core/basic-classes/quadrilateral.html)

### get_referenced_element

Gets a referenced region object element.

```python
def get_referenced_element(self) -> "RegionObjectElement":
```

**Return value**

Returns a referenced `RegionObjectElement` object.

**See Also**

[RegionObjectElement]({{ site.dcvb_python_api }}core/intermediate-results/region-object-element.html)

### get_element_type

Gets the type of the region object element.

```python
def get_element_type(self) -> int:
```

**Return value**

Returns a `EnumRegionObjectElementType` enum value which represents the type of the region object element.

**See Also**

[EnumRegionObjectElementType]({{ site.dcvb_enumerations }}core/region-object-element-type.html?lang=python)

### set_location

Sets the location of the region object element.

```python
def set_location(self, location: Quadrilateral) -> int:
```

**Parameters**

`location` The location of the region object element.

**Return value**

Returns 0 if success, otherwise an error code.

**See Also**

[Quadrilateral]({{ site.dcvb_python_api }}core/basic-classes/quadrilateral.html)

### Clone

Clones the region object element.

```python
def clone(self) -> "RegionObjectElement":
```

**Return value**

Returns a copy of the region object element.

