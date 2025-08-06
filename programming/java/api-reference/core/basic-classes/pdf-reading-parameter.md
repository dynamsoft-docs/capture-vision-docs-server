---
layout: default-layout
title: PDFReadingParameter Class - Dynamsoft Core Module Java Edition API Reference
description: Definition of PDFReadingParameter class in Dynamsoft Core Module Java Edition.
keywords: pdf reading parameter, java
needAutoGenerateSidebar: true
---

# PDFReadingParameter

The `PDFReadingParameter` class represents the parameters for reading a PDF file. It contains the mode of PDF reading, the DPI (dots per inch) value, and the raster data source type.

## Definition

*Package:* `com.dynamsoft.core.basic_structures`

```java
class PDFReadingParameter
```

## Attributes
  
| Attribute  | Type | Description |
|---------- | ---- |-------------|
| [`mode`](#mode) | *int* | The mode used for PDF reading. This is one of the values of the [EnumPDFReadingMode]({{ site.dcvb_java_api }}core/enum-pdf-reading-mode.html) enumeration. |
| [`dpi`](#dpi) | *int* | The DPI (dots per inch) value. |
| [`rasterDataSource`](#rasterdatasource) | *int* | The raster data source type. This is one of the values of the [EnumRasterDataSource]({{ site.dcvb_java_api }}core/enum-raster-data-source.html) enumeration. |

## Constructors
  
| Constructor | Description |
|---------- | ---- |
| [`PDFReadingParameter()`](#pdfreadingparameter) | Initializes a new instance of the `PDFReadingParameter` class. |

## Attributes

### mode

The mode used for PDF reading.

```java
public @EnumPDFReadingMode int mode
```

### dpi

The DPI (dots per inch) value.

```java
public int dpi
```

### rasterDataSource

The raster data source type.

```java
public @EnumRasterDataSource int rasterDataSource
```

## Constructors

### PDFReadingParameter

Initializes a new instance of the `PDFReadingParameter` class.

```java
PDFReadingParameter()
```

**Remarks**

This constructor initializes the attributes with default values:
- `mode`: `EnumPDFReadingMode.PDFRM_RASTER`
- `dpi`: 300
- `rasterDataSource`: `EnumRasterDataSource.RDS_RASTERIZED_PAGES`

