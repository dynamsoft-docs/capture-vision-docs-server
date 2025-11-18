---
layout: default-layout
title: class CImageProcessingModule - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the C++ edition of the class CImageProcessingModule in Dynamsoft Utility Module.
keywords: image processing module, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: C++ CImageProcessingModule Class
---

# CImageProcessingModule

The `CImageProcessingModule` class defines general functions in the image processing module.

## Definition

*Namespace:* dynamsoft::dip

*Assembly:* DynamsoftImageProcessing

```cpp
class CImageProcessingModule 
```

## Methods

| Method                                                    | Description                                        |
| --------------------------------------------------------- | -------------------------------------------------- |
| [GetVersion](#getversion)                                     | Returns the version of the image processing module. |
| [CreatePredetectedRegionElement](#createpredetectedregionelement) | Create a Predetected Region Element object |

## CreatePredetectedRegionElement

Create a Predetected Region Element object

```cpp
static CPredetectedRegionElement* CreatePredetectedRegionElement();
```

**Return Value**

Returns an instance of CPredetectedRegionElement.

## GetVersion

Returns the version of the image processing module.

```cpp
static const char* GetVersion();
```

**Return Value**

Returns a const char pointer representing the version of the image processing module.
