---
layout: default-layout
title: class IdentityProcessor - Dynamsoft Identity Utility Module .NET Edition API Reference
description: This page shows the .NET Edition of the class IdentityProcessor in Dynamsoft Identity Utility Module.
keywords: identity processor, .NET
---

# IdentityProcessor

The `IdentityProcessor` class provides functions to process identity documents, such as locating portrait zones with higher precision.

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

## Definition

*Namespace:* Dynamsoft.IdUtility

```csharp
public class IdentityProcessor
```

## Methods

| Method                                                    | Description                                        |
| --------------------------------------------------------- | -------------------------------------------------- |
| [`IdentityProcessor`](#identityprocessor)                 | Constructor. Initializes a new instance of the `IdentityProcessor` class. |
| [`FindPortraitZone`](#findportraitzone)                   | Finds the location of the portrait zone on an identity document. |

### IdentityProcessor

Constructor. Initializes a new instance of the `IdentityProcessor` class.

```csharp
IdentityProcessor()
```

### FindPortraitZone

Finds the location of the portrait zone on an identity document.

```csharp
int FindPortraitZone(ScaledColourImageUnit scaledColourImgUnit,
                     LocalizedTextLinesUnit localizedTextLinesUnit,
                     RecognizedTextLinesUnit recognizedTextLinesUnit,
                     DetectedQuadsUnit detectedQuadsUnit,
                     DeskewedImageUnit deskewedImageUnit,
                     out Quadrilateral portraitZone)
```

**Parameters**

`[in] scaledColourImgUnit` The scaled colour image unit containing the source image.

`[in] localizedTextLinesUnit` The localized text lines unit containing MRZ/text regions.

`[in] recognizedTextLinesUnit` The recognized text lines unit for document type identification.

`[in] detectedQuadsUnit` The detected quads unit containing document boundaries.

`[in] deskewedImageUnit` The deskewed image unit for coordinate transformation.

`[out] portraitZone` The output quadrilateral representing the portrait zone location. Returns an empty quadrilateral if not found.

**Return value**

Returns 0 if successful, otherwise returns an error code.

**See Also**

[ScaledColourImageUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/scaled-colour-image-unit.html)

[LocalizedTextLinesUnit]({{ site.dlr_dotnet_api }}localized-text-lines-unit.html)

[RecognizedTextLinesUnit]({{ site.dlr_dotnet_api }}recognized-text-lines-unit.html)

[DetectedQuadsUnit]({{ site.ddn_dotnet_api }}detected-quads-unit.html)

[DeskewedImageUnit]({{ site.ddn_dotnet_api }}deskewed-image-unit.html)

[Quadrilateral]({{ site.dcvb_dotnet_api }}core/basic-classes/quadrilateral.html)
