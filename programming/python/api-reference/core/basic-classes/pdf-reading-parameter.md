---
layout: default-layout
title: PDFReadingParameter Class - Dynamsoft Core Module Python Edition API Reference
description: Definition of PDFReadingParameter class in Dynamsoft Core Module Python Edition.
keywords: pdf reading parameter, python
needAutoGenerateSidebar: true
---

# PDFReadingParameter

The `PDFReadingParameter` class represents the parameters for reading a PDF file. It contains the mode of PDF reading, the DPI (dots per inch) value, and the raster data source type.

## Definition

*Module:* dynamsoft_core

```python
class PDFReadingParameter(object)
```

## Properties
  
| Property  | Type | Description |
|---------- | ---- |-------------|
| [`mode`](#mode) | *int* | The mode used for PDF reading. This is one of the values of the [EnumPDFReadingMode]({{ site.dcvb_enumerations }}core/pdf-reading-mode.html?lang=python) enumeration. |
| [`dpi`](#dpi) | *int* | The DPI (dots per inch) value. |
| [`raster_data_source`](#raster_data_source) | *int* | The raster data source type. This is one of the values of the [EnumRasterDataSource]({{ site.dcvb_enumerations }}core/raster-data-source.html?lang=python) enumeration. |

## Methods
  
| Method | Description |
|---------- | ---- |
| [`__init__`](#__init__) | Initializes a new instance of the `PDFReadingParameter` class. |

### \_\_init\_\_

Initializes a new instance of the `PDFReadingParameter` class.

```python
def __init__(self):
```

**Remarks**

This constructor initializes the properties with default values:
- `mode`: 2 (EnumPDFReadingMode.PDFRM_RASTER.value)
- `dpi`: 300
- `raster_data_source`: 0 (EnumRasterDataSource.RDS_RASTERIZED_PAGES.value)

