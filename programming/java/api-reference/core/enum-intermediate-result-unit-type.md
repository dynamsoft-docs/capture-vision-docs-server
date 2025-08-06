---
layout: default-layout
title: IntermediateResultUnitType - Dynamsoft Core Java Enumerations
description: The enumeration IntermediateResultUnitType of Dynamsoft Core describes the type of intermediate result unit.
keywords: Intermediate result unit type
codeAutoHeight: true
---

# Enumeration IntermediateResultUnitType

`IntermediateResultUnitType` describes the type of intermediate result unit.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumIntermediateResultUnitType {
    //No intermediate result.
    long IRUT_NULL = 0;
    //The colour image.
    long IRUT_COLOUR_IMAGE = 1;
    //The scaled colour image.
    long IRUT_SCALED_COLOUR_IMAGE = 1 << 1;
    //The grayscale image.
    long IRUT_GRAYSCALE_IMAGE = 1 << 2;
    //The transformed grayscale image.
    long IRUT_TRANSFORMED_GRAYSCALE_IMAGE = 1 << 3;
    //The enhanced grayscale image.
    long IRUT_ENHANCED_GRAYSCALE_IMAGE = 1 << 4;
    //The predetected regions.
    long IRUT_PREDETECTED_REGIONS = 1 << 5;
    //The binary image.
    long IRUT_BINARY_IMAGE = 1 << 6;
    //The texture detection result.
    long IRUT_TEXTURE_DETECTION_RESULT = 1 << 7;
    //The texture-removed grayscale image.
    long IRUT_TEXTURE_REMOVED_GRAYSCALE_IMAGE = 1 << 8;
    //The texture-removed binary image.
    long IRUT_TEXTURE_REMOVED_BINARY_IMAGE = 1 << 9;
    //The contours.
    long IRUT_CONTOURS = 1 << 10;
    //The line segments.
    long IRUT_LINE_SEGMENTS = 1 << 11;
    //The text zones.
    long IRUT_TEXT_ZONES = 1 << 12;
    //The text-removed binary image.
    long IRUT_TEXT_REMOVED_BINARY_IMAGE = 1 << 13;
    //The candidate barcode zones.
    long IRUT_CANDIDATE_BARCODE_ZONES = 1 << 14;
    //The localized barcodes.
    long IRUT_LOCALIZED_BARCODES = 1 << 15;
    //The scaled barcode image.
    long IRUT_SCALED_BARCODE_IMAGE = 1 << 16;
    //The deformation-resisted barcode image.
    long IRUT_DEFORMATION_RESISTED_BARCODE_IMAGE = 1 << 17;
    //The complemented barcode image.
    long IRUT_COMPLEMENTED_BARCODE_IMAGE = 1 << 18;
    //The decoded barcodes.
    long IRUT_DECODED_BARCODES = 1 << 19;
    //The long lines.
    long IRUT_LONG_LINES = 1 << 20;
    //The corners.
    long IRUT_CORNERS = 1 << 21;
    //The candidate quadrilateral edges.
    long IRUT_CANDIDATE_QUAD_EDGES = 1 << 22;
    //The detected quadrilaterals.
    long IRUT_DETECTED_QUADS = 1 << 23;
    //The localized text lines.
    long IRUT_LOCALIZED_TEXT_LINES = 1 << 24;
    //The recognized text lines.
    long IRUT_RECOGNIZED_TEXT_LINES = 1 << 25;
    //The deskewed image.
    long IRUT_DESKEWED_IMAGE = 1 << 26;
    //The short lines.
    long IRUT_SHORT_LINES = 1 << 27;
    //The raw text lines.
    long IRUT_RAW_TEXT_LINES = 1 << 28;
    //The logic lines.
    long IRUT_LOGIC_LINES = 1 << 29;
    //The enhanced image.
    long IRUT_ENHANCED_IMAGE = 1 << 30;
    //All intermediate result types.
    long IRUT_ALL = 0xFFFFFFFFFFFFFFFFl;
}
```