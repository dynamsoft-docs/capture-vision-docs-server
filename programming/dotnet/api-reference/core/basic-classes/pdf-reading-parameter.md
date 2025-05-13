---
layout: default-layout
title: PDFReadingParameter Class - Dynamsoft Core Module .NET Edition API Reference
description: Definition of PDFReadingParameter class in Dynamsoft Core Module .NET Edition.
keywords: pdf reading parameter, .NET
needAutoGenerateSidebar: true
---

# PDFReadingParameter

The `PDFReadingParameter` class represents the parameters for reading a PDF file. It contains the mode of PDF reading, the DPI (dots per inch) value, and the raster data source type.

## Definition

*Namespace:* Dynamsoft.Core


```csharp
public class PDFReadingParameter 
```

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`mode`](#mode) | *PDFReadingMode* |
| [`dpi`](#dpi) | *int* |
| [`rasterDataSource`](#rasterdatasource) | *RasterDataSource* |

### mode

The mode of PDF reading.

```csharp
EnumPDFReadingMode mode;
```

**See Also**

[EnumPDFReadingMode]({{ site.dcvb_dotnet_api }}core/enum-pdf-reading-mode.html)

### dpi

The DPI (dots per inch) value.

```csharp
int dpi;
```

### rasterDataSource

The raster data source type.

```csharp
EnumRasterDataSource rasterDataSource;
```

**See Also**

[EnumRasterDataSource]({{ site.dcvb_dotnet_api }}core/enum-raster-data-source.html)


## Methods
  
| Method | Description |
|---------- | ---- |
| [`PDFReadingParameter`](#pdfreadingparameter) | Default constructor of a `PDFReadingParameter` object. |
| [`Dispose`](#dispose) | Releases all resources used by current object. |

### PDFReadingParameter

Default constructor of a `PDFReadingParameter` object.

```csharp
PDFReadingParameter()
```

**Remarks**

This constructor initializes the attributes with default values:
- `mode`: EnumPDFReadingMode.PDFRM_RASTER
- `dpi`: 300
- `rasterDataSource`: EnumRasterDataSource.RDS_RASTERIZED_PAGES

### Dispose

Releases all resources used by current object.

```csharp
void Dispose()
```
