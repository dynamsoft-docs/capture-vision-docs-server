---
layout: default-layout
title: PDFReadingMode - Dynamsoft Core .NET Enumerations
description: The enumeration PDFReadingMode describes all available PDF reading modes for .NET Edition.
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
   /** Outputs vector data found in the PDFs. */
   PDFRM_VECTOR = 0x01,
   /** The default value.
    * Outputs raster data found in the PDFs.
    * Depending on the argument Resolution, the SDK may rasterize the PDF pages.
    * Check the template for available argument settings. */
   PDFRM_RASTER = 0x02,
   /** Reserved setting for PDF reading mode.*/
   PDFRM_REV = -2147483648,
}
```