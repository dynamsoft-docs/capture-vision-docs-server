---
layout: default-layout
title: class AuxiliaryRegionElement - Dynamsoft Core Module Python Edition API Reference
description: This page shows the Python edition of the class AuxiliaryRegionElement in Dynamsoft Core Module.
keywords: auxiliary region element, python
---

# AuxiliaryRegionElement

The `AuxiliaryRegionElement` class represents an auxiliary region element that contains additional region information detected during processing (e.g., MRZ, portrait zones, signature areas). It inherits from the `RegionObjectElement` class.

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

## Definition

*Module:* core

*Inheritance:* [RegionObjectElement]({{ site.dcvb_python_api }}core/intermediate-results/region-object-element.html) -> AuxiliaryRegionElement

```python
class AuxiliaryRegionElement(RegionObjectElement)
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `AuxiliaryRegionElement` class. |
| [`get_name`](#get_name) | Gets the name of this auxiliary region. |
| [`get_confidence`](#get_confidence) | Gets the confidence level of this auxiliary region detection. |
| [`set_name`](#set_name) | Sets the name of this auxiliary region. |
| [`set_location`](#set_location) | Sets the location of this auxiliary region. |
| [`set_confidence`](#set_confidence) | Sets the confidence level of this auxiliary region detection. |
| **Methods Inherited from [RegionObjectElement]({{ site.dcvb_python_api }}core/intermediate-results/region-object-element.html):** | |
| [`get_location`]({{ site.dcvb_python_api }}core/intermediate-results/region-object-element.html#get_location) | Gets the location of the region object element. |
| [`get_referenced_element`]({{ site.dcvb_python_api }}core/intermediate-results/region-object-element.html#get_referenced_element) | Gets a referenced region object element. |
| [`get_element_type`]({{ site.dcvb_python_api }}core/intermediate-results/region-object-element.html#get_element_type) | Gets the type of the region object element. |
| [`get_image_data`]({{ site.dcvb_python_api }}core/intermediate-results/region-object-element.html#get_image_data) | Gets the imageData of the region object element. |
| [`clone`]({{ site.dcvb_python_api }}core/intermediate-results/region-object-element.html#clone) | Clones the region object element. |

### \_\_init\_\_

Initializes a new instance of the `AuxiliaryRegionElement` class.

```python
def __init__(self):
```

### get_name

Gets the name of this auxiliary region.

```python
def get_name(self) -> str:
```

**Return value**

Returns a string representing the region name (e.g., "PortraitZone", "SignatureArea").

### get_confidence

Gets the confidence level of this auxiliary region detection.

```python
def get_confidence(self) -> int:
```

**Return value**

Returns the confidence value, typically in the range [0, 100].

### set_name

Sets the name of this auxiliary region.

```python
def set_name(self, name: str) -> None:
```

**Parameters**

`name` The region name to set (e.g., "PortraitZone", "SignatureArea").

### set_location

Sets the location of this auxiliary region.

```python
def set_location(self, location: Quadrilateral) -> int:
```

**Parameters**

`location` A `Quadrilateral` object defining the region boundaries.

**Return value**

Returns 0 if successful, otherwise returns an error code.

**See Also**

[Quadrilateral]({{ site.dcvb_python_api }}core/basic-classes/quadrilateral.html)

### set_confidence

Sets the confidence level of this auxiliary region detection.

```python
def set_confidence(self, confidence: int) -> None:
```

**Parameters**

`confidence` The confidence value to set, typically in the range [0, 100].
