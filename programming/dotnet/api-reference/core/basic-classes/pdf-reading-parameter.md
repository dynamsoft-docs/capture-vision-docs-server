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

*Assembly:* Dynamsoft.Core.dll

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

[EnumPDFReadingMode]({{ site.dcv_enumerations }}core/pdf-reading-mode.html?lang=dotnet)

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

[EnumRasterDataSource]({{ site.dcv_enumerations }}core/raster-data-source.html?lang=dotnet)


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
