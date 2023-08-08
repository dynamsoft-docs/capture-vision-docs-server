---
layout: default-layout
title: class CPDFReadingParameter - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CPDFReadingParameter in Dynamsoft Core Module.
keywords: pdf reading parameter, c++
needAutoGenerateSidebar: true
permalink: /programming/cplusplus/api-reference/core/basic-structures/pdf-reading-parameter-v2.0.0.html
---

# CPDFReadingParameter

The CPDFReadingParameter class represents the parameters for reading a PDF file. It contains the mode of PDF reading, the DPI (dots per inch) value, and the tarGetstype.

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
| [`type`](#type) | *TargetType* |

### mode

The mode of PDF reading.

```cpp
PDFReadingMode mode
```

### dpi

The DPI (dots per inch) value.

```cpp
int dpi
```

### type

The target type.

```cpp
TargetType type
```
