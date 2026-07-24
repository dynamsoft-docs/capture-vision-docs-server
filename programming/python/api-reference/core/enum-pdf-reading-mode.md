---
layout: default-layout
title: PDFReadingMode - Dynamsoft Core Python Enumerations
description: The enumeration PDFReadingMode in Dynamsoft Core Python Edition lists the available modes for reading PDF files (raster, vector, auto).
keywords: PDF Reading Mode
codeAutoHeight: true
---

# Enumeration PDFReadingMode

`PDFReadingMode` describes the PDF reading modes.

```python
class EnumPDFReadingMode(IntEnum):
    # Deprecated. Covered by PDFRM_MULTIMODAL.
    PDFRM_VECTOR = 0x01
    # Renders the entire page as a bitmap regardless of object type.
    PDFRM_RASTER = 0x02
    # Extracts multimodal information from a PDF, including vector graphics,
    # text content, and embedded images.
    PDFRM_MULTIMODAL = 0x03
    PDFRM_REV = -2147483648
```