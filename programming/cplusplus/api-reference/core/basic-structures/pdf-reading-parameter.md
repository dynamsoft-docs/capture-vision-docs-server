---
layout: default-layout
title: class CPDFReadingParameter - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CPDFReadingParameter in Dynamsoft Core Module.
keywords: pdf reading parameter, c++
needAutoGenerateSidebar: true
---

# CPDFReadingParameter

The `CPDFReadingParameter` class represents the parameters for reading a PDF file. It contains the mode of PDF reading, the DPI (dots per inch) value, and the raster data source type.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore

```cpp
class CPDFReadingParameter 
```

## Attributes Summary
  
| Attribute | Type |
|---------- | ---- |
| [`mode`](#mode) | *PDFReadingMode* |
| [`dpi`](#dpi) | *int* |
| [`rasterDataSource`](#rasterdatasource) | *RasterDataSource* |

### mode

The mode of PDF reading.

```cpp
PDFReadingMode mode
```

**See Also**

[PDFReadingMode]({{ site.dcvb_enumerations }}core/pdf-reading-mode.html?src=cpp&&lang=cpp)

### dpi

The DPI (dots per inch) value.

```cpp
int dpi
```

### rasterDataSource

The raster data source type.

```cpp
RasterDataSource rasterDataSource
```

**See Also**

[RasterDataSource]({{ site.dcvb_enumerations }}core/raster-data-source.html?src=cpp&&lang=cpp)

