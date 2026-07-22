---
layout: default-layout
title: PDFReadingMode - Dynamsoft Core .NET Enumerations
description: The enumeration PDFReadingMode in Dynamsoft Core .NET Edition lists the available modes for reading PDF files (raster, vector, auto).
keywords: PDF Reading Mode
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
codeAutoHeight: true
---

# Enumeration PDFReadingMode

`PDFReadingMode` describes the PDF reading modes.

```csharp
public enum EnumPDFReadingMode
{
   /** Deprecated. Covered by PDFRM_MULTIMODAL. */
   PDFRM_VECTOR = 0x01,
   /** Renders the entire page as a bitmap regardless of object type. */
   PDFRM_RASTER = 0x02,
   /**
    * Extracts multimodal information from a PDF, including vector graphics,
    * text content, and embedded images, which can be used for subsequent
    * tasks such as barcode reading, text recognition, and document analysis.
    */
   PDFRM_MULTIMODAL = 0x03,
   /** Reserved setting for PDF reading mode.*/
   PDFRM_REV = -2147483648,
}
```