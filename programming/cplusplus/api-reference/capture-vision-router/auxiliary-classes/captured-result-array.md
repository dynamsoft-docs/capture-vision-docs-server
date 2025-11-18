---
layout: default-layout
title: class CCapturedResultArray - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the C++ edition of the class CCapturedResultArray in Dynamsoft Capture Vision Router Module.
keywords: captured result array, c++
needAutoGenerateSidebar: true
---

# CCapturedResultArray

The `CCapturedResultArray` class represents a collection of captured results, each derived from a capture operation on an image. Internally, `CaptureResult` maintains an array of items, which may include barcodes, text lines, detected quads, normalized images, raw images, parsed items, and more.

## Definition

*Namespace:* dynamsoft::cvr

*Assembly:* DynamsoftCaptureVisionRouter

```cpp
class CCapturedResultArray 
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetResultsCount`](#getresultscount) | Gets the number of [`CCapturedResult`]({{ site.dcvb_cpp_api }}capture-vision-router/auxiliary-classes/captured-result.html) objects in the array.|
| [`GetResult`](#getresult) | Gets a pointer to the [`CCapturedResult`]({{ site.dcvb_cpp_api }}capture-vision-router/auxiliary-classes/captured-result.html) object at the specified index.|
| [`operator[]`](#operator) | Gets a pointer to the [`CCapturedResult`]({{ site.dcvb_cpp_api }}capture-vision-router/auxiliary-classes/captured-result.html) object at the specified index. |
| [`Retain`](#retain) | Increases the reference count of the `CCapturedResultArray` object.|
| [`Release`](#release) | Decreases the reference count of the `CCapturedResultArray` object.|

### GetResultsCount

Gets the number of [`CCapturedResult`]({{ site.dcvb_cpp_api }}capture-vision-router/auxiliary-classes/captured-result.html) objects in the array.

```cpp
int GetItemsCount() const
```

**Return value**

Returns the number of [`CCapturedResult`]({{ site.dcvb_cpp_api }}capture-vision-router/auxiliary-classes/captured-result.html) objects in the array.

### GetResult

Gets a pointer to the [`CCapturedResult`]({{ site.dcvb_cpp_api }}capture-vision-router/auxiliary-classes/captured-result.html) object at the specified index.

```cpp
const CCapturedResult* GetResult(int index) const
```

**Parameters**

`[in] index` The index of the result to retrieve.

**Return value**

Returns a pointer to the [`CCapturedResult`]({{ site.dcvb_cpp_api }}capture-vision-router/auxiliary-classes/captured-result.html) object.

**See Also**

[CCapturedResult]({{ site.dcvb_cpp_api }}capture-vision-router/auxiliary-classes/captured-result.html)

### operator[]

Gets a pointer to the [`CCapturedResult`]({{ site.dcvb_cpp_api }}capture-vision-router/auxiliary-classes/captured-result.html) object at the specified index.

```cpp
virtual const CCapturedResult* operator[](int index) const = 0;
```

**Parameters**

`[in] index` The index of the result to retrieve.

**Return value**

Returns a pointer to the [`CCapturedResult`]({{ site.dcvb_cpp_api }}capture-vision-router/auxiliary-classes/captured-result.html) object.

### Retain

Increases the reference count of the `CCapturedResultArray` object.

```cpp
virtual CCapturedResultArray* Retain() = 0;
```

**Return value**

Return an object of `CCapturedResultArray`.

### Release

Decreases the reference count of the `CCapturedResultArray` object.

```cpp
virtual void Release() = 0;
```
