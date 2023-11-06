---
layout: default-layout
title: class COriginalImageResultItem - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the C++ edition of the class COriginalImageResultItem in Dynamsoft Capture Vision Router Module.
keywords: original image, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: CVR C++ COriginalImageResultItem Class
permalink: /programming/cplusplus/api-reference/core/basic-structures/original-image-result-item.html
---

# COriginalImageResultItem

The `COriginalImageResultItem` class represents a captured original image result item. It is a derived class of `CCapturedResultItem` and provides an interface to get the image data.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore

```cpp
class COriginalImageResultItem: public CCapturedResultItem
```

## Methods Summary

| Method                          | Description                                      |
| ------------------------------- | ------------------------------------------------ |
| [`GetImageData`](#getimagedata) | Gets the image data for the COriginalImageResultItem. |

### Inherited Methods

{%- include inherited-methods/captured-result-item.md -%}

### GetImageData

Gets the image data for the COriginalImageResultItem.

```cpp
virtual const CImageData* GetImageData() const = 0;
```

**Return value**

Returns a const pointer to the CImageData object that contains the image data for the COriginalImageResultItem.
