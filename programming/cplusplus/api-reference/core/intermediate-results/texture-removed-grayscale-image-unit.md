---
layout: default-layout
title: class CTextureRemovedGrayscaleImageUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CTextureRemovedGrayscaleImageUnit in Dynamsoft Core Module.
keywords: text removed grayscale image, c++
needAutoGenerateSidebar: true
---

# CTextureRemovedGrayscaleImageUnit

The CTextureRemovedGrayscaleImageUnit class represents an intermediate result unit that contains texture-removed grayscale image data.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore

```cpp
class CTextureRemovedGrayscaleImageUnit : public CIntermediateResultUnit 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets the texture-removed grayscale image.|

### Inherited Methods

{%- include inherited-methods/intermediate-result-unit.md -%}

### GetImageData

Gets the texture-removed grayscale image.

```cpp
virtual const CImageData* GetImageData() const
```

**Return value**

Returns a constant pointer to the texture-removed grayscale image. You don't need to release the memory pointed to by the returned pointer.
