---
layout: default-layout
title: RasterDataSource - Dynamsoft Core Enumerations
description: Reference for the RasterDataSource enumeration in Dynamsoft Core C++ Edition, specifying whether raster image data comes from pages or rendered PDFs.
keywords: Target type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RasterDataSource
---

# Enumeration RasterDataSource

`RasterDataSource` describes the target types.

<div class="sample-code-prefix template2"></div>
   >- C++
   >
>
```cpp
typedef enum RasterDataSource
{
   /**The raster data source type of the PDF file is "pages". Only available for PDFReadingMode PDFRM_RASTER.*/
   RDS_RASTERIZED_PAGES,
   /**The raster data source type of the PDF file is "images".*/
   RDS_EXTRACTED_IMAGES
} RasterDataSource;
```