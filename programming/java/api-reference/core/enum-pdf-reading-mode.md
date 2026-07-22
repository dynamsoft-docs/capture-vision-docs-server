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
    /** Deprecated. Covered by PDFRM_MULTIMODAL. */
    int PDFRM_VECTOR = 0x01;
    /** Renders the entire page as a bitmap regardless of object type. */
    int PDFRM_RASTER = 0x02;
    /**
     * Extracts multimodal information from a PDF, including vector graphics,
     * text content, and embedded images, which can be used for subsequent
     * tasks such as barcode reading, text recognition, and document analysis.
     */
    int PDFRM_MULTIMODAL = 0x03;
    /** Reserved PDF reading mode. */
    int PDFRM_REV = 0x80000000;
}
```