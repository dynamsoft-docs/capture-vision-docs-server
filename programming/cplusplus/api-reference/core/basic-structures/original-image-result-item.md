---
layout: default-layout
title: class COriginalImageResultItem - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the C++ edition of the class COriginalImageResultItem in Dynamsoft Capture Vision Router Module.
keywords: original image, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: CVR C++ COriginalImageResultItem Class
---

# COriginalImageResultItem

The `COriginalImageResultItem` class represents a captured original image result item. It is a derived class of `CCapturedResultItem` and provides an interface to get the image data.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore

*Inheritance:* [CCapturedResultItem]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html) -> COriginalImageResultItem

```cpp
class COriginalImageResultItem: public CCapturedResultItem
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetImageData`](#getimagedata) | Gets the image data for the `COriginalImageResultItem`. |
| **Methods Inherited from [CCapturedResultItem]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html):** | |
| [`GetType`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#gettype) | Gets the type of the captured result item. |
| [`GetReferenceItem`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#getreferenceitem) | Gets a pointer to the referenced item in the captured result item. |
| [`GetTargetROIDefName`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#gettargetroidefname) | Gets the name of the target ROI definition. |
| [`GetTaskName`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#gettaskname) | Gets the name of the task. |
| [`Retain`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#retain) | Increases the reference count of the captured result item. |
| [`Release`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#release) | Decreases the reference count of the captured result item. |
| [`Clone`]({{ site.dcvb_cpp_api }}core/basic-structures/captured-result-item.html#clone) | Creates a copy of the captured result item. |

### GetImageData

Gets the image data for the `COriginalImageResultItem`.

```cpp
virtual const CImageData* GetImageData() const = 0;
```

**Return value**

Returns a const pointer to the `CImageData` object that contains the image data for the `COriginalImageResultItem`.

**See Also**

[CImageData]({{ site.dcvb_cpp_api }}core/basic-structures/image-data.html)
