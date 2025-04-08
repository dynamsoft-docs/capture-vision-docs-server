---
layout: default-layout
title: RegionObjectElementType - Dynamsoft Core Python Enumerations
description: The enumeration RegionObjectElementType of Dynamsoft Core describes the types of RegionObjectElement.
keywords: Region object element type
codeAutoHeight: true
---

# Enumeration RegionObjectElementType

`RegionObjectElementType` specifies the exact subclass type within the `RegionObjectElement` hierarchy. This enumeration facilitates the identification and differentiation of various processed elements in an image.

```python
class EnumRegionObjectElementType(IntEnum):
   # The type of subclass PredetectedRegionElement.
   ROET_PREDETECTED_REGION
   # The type of subclass LocalizedBarcodeElement.
   ROET_LOCALIZED_BARCODE
   # The type of subclass DecodedBarcodeElement.
   ROET_DECODED_BARCODE
   # The type of subclass LocalizedTextLineElement.
   ROET_LOCALIZED_TEXT_LINE
   # The type of subclass RecognizedTextLineElement.
   ROET_RECOGNIZED_TEXT_LINE
   # The type of subclass DetectedQuadElement.
   ROET_DETECTED_QUAD
   # The type of subclass NormalizedImageElement.
   ROET_NORMALIZED_IMAGE
   # The type of subclass SourceImageElement.
   ROET_SOURCE_IMAGE
   # The type of subclass TargetROIElement.
   ROET_TARGET_ROI
```