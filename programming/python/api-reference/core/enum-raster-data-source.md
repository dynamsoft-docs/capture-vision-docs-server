---
layout: default-layout
title: RasterDataSource - Dynamsoft Core Python Enumerations
description: The enumeration RasterDataSource of Dynamsoft Core describes raster data source types.
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