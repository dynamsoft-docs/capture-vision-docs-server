---
layout: default-layout
title: PDFReadingMode - Dynamsoft Core Java Enumerations
description: The enumeration PDFReadingMode in Dynamsoft Core Java Edition lists the available modes for reading PDF files (raster, vector, auto).
keywords: PDF Reading Mode
codeAutoHeight: true
---

# Enumeration PDFReadingMode

`PDFReadingMode` describes the PDF reading modes.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumPDFReadingMode {
    //Vector PDF reading mode.
    int PDFRM_VECTOR = 0x01;
    //Raster PDF reading mode.
    int PDFRM_RASTER = 0x02;
    //Reserved PDF reading mode.
    int PDFRM_REV = 0x80000000;
}
```