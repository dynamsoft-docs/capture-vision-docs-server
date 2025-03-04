---
layout: default-layout
title: SectionType - Dynamsoft Core Enumerations
description: The enumeration SectionType of Dynamsoft Core describes the section of the algorithm.
keywords: Section type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: SectionType
codeAutoHeight: true
---

# Enumeration SectionType

`SectionType` categorizes the distinct segments within the image processing algorithm, pinpointing the exact phase responsible for generating a specific `IntermediateResult`.


<div class="sample-code-prefix template2"></div>
   >- C++
   >
>
```cpp
typedef enum SectionType
{
   /**No section type is specified.*/
   ST_NULL,
   /**The result is output by "region prediction" section.*/
   ST_REGION_PREDETECTION,
   /**The result is output by "barcode localization" section.*/
   ST_BARCODE_LOCALIZATION,
   /**The result is output by "barcode decoding" section.*/
   ST_BARCODE_DECODING,
   /**The result is output by "text line localization" section.*/
   ST_TEXT_LINE_LOCALIZATION,
   /**The result is output by "text line  recognition" section.*/
   ST_TEXT_LINE_RECOGNITION,
   /**The result is output by "document detection" section.*/
   ST_DOCUMENT_DETECTION,
   /**The result is output by "document deskewing" section.*/
   ST_DOCUMENT_DESKEWING,
   /**The result is output by "image enhancement" section.*/
   ST_IMAGE_ENHANCEMENT
} SectionType;
```