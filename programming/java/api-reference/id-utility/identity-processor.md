---
layout: default-layout
title: class IdentityProcessor - Dynamsoft Identity Utility Module Java Edition API Reference
description: This page shows the Java edition of the class IdentityProcessor in Dynamsoft Identity Utility Module.
keywords: identity processor, java
---

# IdentityProcessor

The `IdentityProcessor` class provides functions to process identity documents, such as locating portrait zones with higher precision.

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

## Definition

*Package:* com.dynamsoft.id_utility

```java
public class IdentityProcessor
```

## Methods

| Method                                                    | Description                                        |
| --------------------------------------------------------- | -------------------------------------------------- |
| [`IdentityProcessor`](#identityprocessor)                 | Constructor. Initializes a new instance of the `IdentityProcessor` class. |
| [`findPortraitZone`](#findportraitzone)                   | Finds the location of the portrait zone on an identity document. |

### IdentityProcessor

Constructor. Initializes a new instance of the `IdentityProcessor` class.

```java
IdentityProcessor()
```

### findPortraitZone

Finds the location of the portrait zone on an identity document.

```java
Quadrilateral findPortraitZone(ScaledColourImageUnit scaledColourImgUnit,
                               LocalizedTextLinesUnit localizedTextLinesUnit,
                               RecognizedTextLinesUnit recognizedTextLinesUnit,
                               DetectedQuadsUnit detectedQuadsUnit,
                               DeskewedImageUnit deskewedImageUnit) throws IdentityUtilityException
```

**Parameters**

`scaledColourImgUnit` The scaled colour image unit containing the source image.

`localizedTextLinesUnit` The localized text lines unit containing MRZ/text regions.

`recognizedTextLinesUnit` The recognized text lines unit for document type identification.

`detectedQuadsUnit` The detected quads unit containing document boundaries.

`deskewedImageUnit` The deskewed image unit for coordinate transformation.

**Return value**

Returns a `Quadrilateral` representing the portrait zone location. Returns `null` if not found.

**Exception**

[IdentityUtilityException]({{ site.dcvb_java_api }}id-utility/identity-utility-exception.html)

**See Also**

[ScaledColourImageUnit]({{ site.dcvb_java_api }}core/intermediate-results/scaled-colour-image-unit.html)

[LocalizedTextLinesUnit]({{ site.dlr_java_api }}localized-text-lines-unit.html)

[RecognizedTextLinesUnit]({{ site.dlr_java_api }}recognized-text-lines-unit.html)

[DetectedQuadsUnit]({{ site.ddn_java_api }}detected-quads-unit.html)

[DeskewedImageUnit]({{ site.ddn_java_api }}deskewed-image-unit.html)

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)
