---
layout: default-layout
title: CapturedResultItemType - Dynamsoft Core Enumerations
description: The enumeration CapturedResultItemType of Dynamsoft Core describes all types of captured result item.
keywords: Captured result types
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CapturedResultItemType
codeAutoHeight: true
---

# Enumeration CapturedResultItemType

`CapturedResultItemType` defines the various categories of items that can be recognized and captured.

<div class="sample-code-prefix template2"></div>
   >- C++
   >
>
```cpp
typedef enum CapturedResultItemType
{
   /** The type of the CapturedResultItem is "original image". */
   CRIT_ORIGINAL_IMAGE = 1,
   /** The type of the CapturedResultItem is "barcode". */
   CRIT_BARCODE = 2,
   /** The type of the CapturedResultItem is "text line". */
   CRIT_TEXT_LINE = 4,
   /** The type of the CapturedResultItem is "detected quad". */
   CRIT_DETECTED_QUAD = 8,
   /** The type of the CapturedResultItem is "normalized image". */
   CRIT_DESKEWED_IMAGE = 16,
   /** The type of the CapturedResultItem is "parsed result". */
   CRIT_PARSED_RESULT = 32,
   /** The type of the CapturedResultItem is "enhanced image". */
   CRIT_ENHANCED_IMAGE = 64
} CapturedResultItemType;
```