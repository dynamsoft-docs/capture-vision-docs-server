---
layout: default-layout
title: RegionObjectElementType - Dynamsoft Core Java Enumerations
description: The enumeration RegionObjectElementType of Dynamsoft Core describes the types of RegionObjectElement.
keywords: Region object element type
codeAutoHeight: true
---

# Enumeration RegionObjectElementType

`RegionObjectElementType` specifies the exact subclass type within the `RegionObjectElement` hierarchy. This enumeration facilitates the identification and differentiation of various processed elements in an image.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumRegionObjectElementType {
    //The type of subclass PredetectedRegionElement.
    int ROET_PREDETECTED_REGION = 0;
    //The type of subclass LocalizedBarcodeElement.
    int ROET_LOCALIZED_BARCODE = 1;
    //The type of subclass DecodedBarcodeElement.
    int ROET_DECODED_BARCODE = 2;
    //The type of subclass LocalizedTextLineElement.
    int ROET_LOCALIZED_TEXT_LINE = 3;
    //The type of subclass RecognizedTextLineElement.
    int ROET_RECOGNIZED_TEXT_LINE = 4;
    //The type of subclass DetectedQuadElement.
    int ROET_DETECTED_QUAD = 5;
    //The type of subclass DeskewedImageElement.
    int ROET_DESKEWED_IMAGE = 6;
    //The type of subclass SourceImageElement.
    int ROET_SOURCE_IMAGE = 7;
    //The type of subclass TargetROIElement.
    int ROET_TARGET_ROI = 8;
    //The type of subclass EnhancedImageElement.
    int ROET_ENHANCED_IMAGE = 9;
    //The type of subclass AuxiliaryRegionElement.
    int ROET_AUXILIARY_REGION = 10;
}
```