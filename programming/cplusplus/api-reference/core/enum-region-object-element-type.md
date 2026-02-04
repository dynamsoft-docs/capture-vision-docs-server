---
layout: default-layout
title: RegionObjectElementType - Dynamsoft Core Enumerations
description: The enumeration RegionObjectElementType of Dynamsoft Core describes the types of RegionObjectElement.
keywords: Region object element type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RegionObjectElementType
codeAutoHeight: true
---

# Enumeration RegionObjectElementType

`RegionObjectElementType` specifies the exact subclass type within the `RegionObjectElement` hierarchy. This enumeration facilitates the identification and differentiation of various processed elements in an image.

<div class="sample-code-prefix template2"></div>
   >- C++
   >
>
```cpp
typedef enum RegionObjectElementType
{
   /**The type of subclass PredetectedRegionElement.*/
   ROET_PREDETECTED_REGION,
   /**The type of subclass LocalizedBarcodeElement.*/
   ROET_LOCALIZED_BARCODE,
   /**The type of subclass DecodedBarcodeElement.*/
   ROET_DECODED_BARCODE,
   /**The type of subclass LocalizedTextLineElement.*/
   ROET_LOCALIZED_TEXT_LINE,
   /**The type of subclass RecognizedTextLineElement.*/
   ROET_RECOGNIZED_TEXT_LINE,
   /**The type of subclass DetectedQuadElement.*/
   ROET_DETECTED_QUAD,
   /**The type of subclass DeskewedImageElement.*/
   ROET_DESKEWED_IMAGE,
   /**The type of subclass EnhancedImageElement */
   ROET_ENHANCED_IMAGE,
   /**The type of subclass SourceImageElement.*/
   ROET_SOURCE_IMAGE,
   /**The type of subclass TargetROIElement.*/
   ROET_TARGET_ROI,
   /**The type of subclass AuxiliaryRegionElement.*/
   ROET_AUXILIARY_REGION
} RegionObjectElementType;
```