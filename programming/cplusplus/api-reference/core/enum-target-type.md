---
layout: default-layout
title: TargetType - Dynamsoft Core Enumerations
description: The enumeration TargetType of Dynamsoft Core describes target types.
keywords: Target type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: TargetType
codeAutoHeight: true
---

# Enumeration TargetType

`TargetType` describes the target types.

<div class="sample-code-prefix template2"></div>
   >- C++
   >
>
```cpp
typedef enum TargetType
{
   /**The target type of the PDF file is "page". Only available for PDFReadingMode PDFRM_RASTER.*/
   TT_PAGE,
   /**The target type of the PDF file is "image".*/
   TT_IMAGE
} TargetType;
```
