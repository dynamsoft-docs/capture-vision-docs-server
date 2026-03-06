---
layout: default-layout
title: RasterDataSource - Dynamsoft Core Java Enumerations
description: The enumeration RasterDataSource in Dynamsoft Core Java Edition specifies whether raster image data is sourced from pages or rendered PDFs.
keywords: Target type
---

# Enumeration RasterDataSource

`RasterDataSource` describes the target types.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumRasterDataSource {
    //The raster data source type of the PDF file is "pages". Only available for PDFReadingMode PDFRM_RASTER.
    int RDS_RASTERIZED_PAGES = 0;
    //The raster data source type of the PDF file is "images".
    int RDS_EXTRACTED_IMAGES = 1;
}
```