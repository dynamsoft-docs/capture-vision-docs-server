---
layout: default-layout
title: class CIdentityProcessor - Dynamsoft Identity Utility Module C++ Edition API Reference
description: This page shows the C++ edition of the class CIdentityProcessor in Dynamsoft Identity Utility Module.
keywords: identity processor, c++
---

# CIdentityProcessor

The `CIdentityProcessor` class provides functions to process identity documents, such as locating portrait zones with higher precision.

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

## Definition

*Namespace:* dynamsoft::id_utility

*Assembly:* DynamsoftIdentityUtility

```cpp
class CIdentityProcessor
```

## Methods

| Method                                                    | Description                                        |
| --------------------------------------------------------- | -------------------------------------------------- |
| [FindPortraitZone](#findportraitzone)                     | Finds the location of the portrait zone on an identity document. |

### FindPortraitZone

Finds the location of the portrait zone on an identity document.

```cpp
int FindPortraitZone(const CScaledColourImageUnit* scaledColourImgUnit,
                     const CLocalizedTextLinesUnit* localizedTextLinesUnit,
                     const CRecognizedTextLinesUnit* recognizedTextLinesUnit,
                     const CDetectedQuadsUnit* detectedQuadsUnit,
                     const CDeskewedImageUnit* deskewedImageUnit,
                     CQuadrilateral& portraitZone);
```

**Parameters**

`[in] scaledColourImgUnit` The scaled colour image unit containing the source image.

`[in] localizedTextLinesUnit` The localized text lines unit containing MRZ/text regions.

`[in] recognizedTextLinesUnit` The recognized text lines unit for document type identification.

`[in] detectedQuadsUnit` The detected quads unit containing document boundaries.

`[in] deskewedImageUnit` The deskewed image unit for coordinate transformation.

`[out] portraitZone` The output quadrilateral representing the portrait zone location. Returns an empty quadrilateral if not found.

**Return Value**

Returns 0 if successful, otherwise returns an error code.

**See Also**

[CScaledColourImageUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/scaled-colour-image-unit.html)

[CLocalizedTextLinesUnit]({{ site.dlr_cpp_api }}localized-text-lines-unit.html)

[CRecognizedTextLinesUnit]({{ site.dlr_cpp_api }}recognized-text-lines-unit.html)

[CDetectedQuadsUnit]({{ site.ddn_cpp_api }}detected-quads-unit.html)

[CDeskewedImageUnit]({{ site.ddn_cpp_api }}deskewed-image-unit.html)

[CQuadrilateral]({{ site.dcvb_cpp_api }}core/basic-structures/quadrilateral.html)
