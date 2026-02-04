---
layout: default-layout
title: class IdentityProcessor - Dynamsoft Identity Utility Module Python Edition API Reference
description: This page shows the Python edition of the class IdentityProcessor in Dynamsoft Identity Utility Module.
keywords: identity processor, python
---

# IdentityProcessor

The `IdentityProcessor` class provides functions to process identity documents, such as locating portrait zones with higher precision.

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

## Definition

*Module:* id_utility

```python
class IdentityProcessor()
```

## Methods

| Method                                                    | Description                                        |
| --------------------------------------------------------- | -------------------------------------------------- |
| [`__init__`](#__init__)                                   | Initializes a new instance of the `IdentityProcessor` class. |
| [`find_portrait_zone`](#find_portrait_zone)               | Finds the location of the portrait zone on an identity document. |

### \_\_init\_\_

Initializes a new instance of the `IdentityProcessor` class.

```python
def __init__(self):
```

### find_portrait_zone

Finds the location of the portrait zone on an identity document.

```python
def find_portrait_zone(
    self,
    scaled_colour_img_unit: ScaledColourImageUnit,
    localized_text_lines_unit: LocalizedTextLinesUnit,
    recognized_text_lines_unit: RecognizedTextLinesUnit,
    detected_quads_unit: DetectedQuadsUnit,
    deskewed_image_unit: DeskewedImageUnit
) -> Tuple[int, Quadrilateral]:
```

**Parameters**

`scaled_colour_img_unit` The scaled colour image unit containing the source image.

`localized_text_lines_unit` The localized text lines unit containing MRZ/text regions.

`recognized_text_lines_unit` The recognized text lines unit for document type identification.

`detected_quads_unit` The detected quads unit containing document boundaries.

`deskewed_image_unit` The deskewed image unit for coordinate transformation.

**Return value**

Returns a tuple containing:
- `error_code` <*int*>: Returns 0 if successful, otherwise returns an error code.
- `portrait_zone` <*Quadrilateral*>: The quadrilateral representing the portrait zone location. Returns `None` if not found.

**See Also**

[ScaledColourImageUnit]({{ site.dcvb_python_api }}core/intermediate-results/scaled-colour-image-unit.html)

[LocalizedTextLinesUnit]({{ site.dlr_python_api }}localized-text-lines-unit.html)

[RecognizedTextLinesUnit]({{ site.dlr_python_api }}recognized-text-lines-unit.html)

[DetectedQuadsUnit]({{ site.ddn_python_api }}detected-quads-unit.html)

[DeskewedImageUnit]({{ site.ddn_python_api }}deskewed-image-unit.html)

[Quadrilateral]({{ site.dcvb_python_api }}core/basic-classes/quadrilateral.html)
