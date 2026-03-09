---
layout: default-layout
title: RasterDataSource - Dynamsoft Core Python Enumerations
description: The enumeration RasterDataSource in Dynamsoft Core Python Edition specifies whether raster image data is sourced from pages or rendered PDFs.
keywords: Target type
---

# Enumeration RasterDataSource

`RasterDataSource` describes the target types.

```python
class EnumRasterDataSource(IntEnum):
   #The raster data source type of the PDF file is "pages". Only available for PDFReadingMode PDFRM_RASTER.
   RDS_RASTERIZED_PAGES,
   #The raster data source type of the PDF file is "images".
   RDS_EXTRACTED_IMAGES
```