---
layout: default-layout
title: class CCapturedResult - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the C++ edition of the class CCapturedResult in Dynamsoft Capture Vision Router Module.
keywords: captured result, c++
needAutoGenerateSidebar: true
---

# CCapturedResult

The CCapturedResult class represents the result of a capture operation on an image. Internally, CaptureResult stores an array that contains multiple items, each of which may be a barcode, text line, detected quad, normalized image, raw image, parsed item, etc.

## Definition

*Namespace:* dynamsoft::cvr

*Assembly:* DynamsoftCaptureVisionRouter

```cpp
class CCapturedResult 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetOriginalImageHashId`](#getoriginalimagehashid) | Gets the hash ID of the original image.|
| [`GetOriginalImageTag`](#getoriginalimagetag) | Gets the tag of the original image.|
| [`GetItemsCount`](#getitemscount) | Gets the number of items in the captured result.|
| [`GetItem`](#getitem) | Gets a specific item in the captured result.|
| [`HasItem`](#hasitem) | Check if the item is present in the array.|
| [`RemoveItem`](#removeitem) | Remove a specific item from the array in the captured result.|
| [`GetRotationTransformMatrix`](#getrotationtransformmatrix) | Get the rotation transformation matrix of the original image relative to the rotated image.|
| [`GetErrorCode`](#geterrorcode) | Gets the error code of the capture operation.|
| [`GetErrorString`](#geterrorstring) | Gets the error message of the capture operation.|
| [`operator[]`](#operator) | Gets a pointer to the [`CCapturedResultItem`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-item.html) object at the specified index. |
| [`Retain`](#retain) | Increases the reference count of the `CCapturedResult` object.|
| [`Release`](#release) | Decreases the reference count of the `CCapturedResult` object.|
| [`GetDecodedBarcodesResult`](#getdecodedbarcodesresult) | Gets the decoded barcode items from the `CCapturedResult`.|
| [`GetRecognizedTextLinesResult`](#getrecognizedtextlinesresult) | Gets the recognized text line items from the `CCapturedResult`.|
| [`GetDetectedQuadsResult`](#getdetectedquadsresult) | Gets the detected quads items from the `CCapturedResult`.|
| [`GetNormalizedImagesResult`](#getnormalizedimagesresult) | Gets the normalized images items from the `CCapturedResult`.|
| [`GetParsedResult`](#getparsedresult) | Gets the parsed result items from the `CCapturedResult`.|

### GetOriginalImageHashId

Gets the hash ID of the original image.

```cpp
const char* GetOriginalImageHashId() const
```

**Return value**

Returns the hash ID of the original image as a null-terminated string. You are not required to release the memory pointed to by the returned pointer.

### GetOriginalImageTag

Gets the tag of the original image.

```cpp
const CImageTag* GetOriginalImageTag() const
```

**Return value**

Returns a pointer to the `CImageTag` object containing the tag of the original image. You are not required to release the memory pointed to by the returned pointer.

**See Also**

[CImageTag]({{ site.dcv_cpp_api }}core/basic-structures/image-tag.html)

### GetItemsCount

Gets the number of items in the captured result.

```cpp
int GetItemsCount() const
```

**Return value**

Returns the number of items in the captured result.

### GetItem

Gets a specific item in the captured result.

```cpp
const CCapturedResultItem* GetItem(int index) const
```

**Parameters**

`[in] index` The index of the item to retrieve.

**Return value**

Returns a pointer to the [`CCapturedResultItem`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-item.html) object at the specified index.

**See Also**

[CCapturedResultItem]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-item.html)

### HasItem

Check if the item is present in the array.

```cpp
bool HasItem(const CCapturedResultItem* item) const
```

**Parameters**

`[in] item` The specific item to check.

**Return value**

Returns a bool value indicating whether the item is present in the array or not.

**See Also**

[CCapturedResultItem]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-item.html)

### RemoveItem

Remove a specific item from the array in the captured result.

```cpp
int RemoveItem(const CCapturedResultItem* item)
```

**Parameters**

`[in] item` The specific item to remove.

**Return value**

Return value indicating whether the deletion was successful or not.

**See Also**

[CCapturedResultItem]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-item.html)

### GetRotationTransformMatrix

Get the rotation transformation matrix of the original image relative to the rotated image.

```cpp
void GetRotationTransformMatrix(double matrix[9]) const;
```

**Parameters**

`[out] matrix` A double array which represents the rotation transform matrix.

### GetErrorCode

Gets the error code of the capture operation.

```cpp
int GetErrorCode() const
```

**Return value**

Returns the error code of the capture operation.

**See Also**

[ErrorCode]({{ site.dcv_enumerations }}core/error-code.html?src=cpp&&lang=cpp)

### GetErrorString

Gets the error message of the capture operation.

```cpp
const char* GetErrorString() const
```

**Return value**

Returns the error message of the capture operation as a null-terminated string. You are not required to release the memory pointed to by the returned pointer.

### operator[]

Gets a pointer to the [`CCapturedResultItem`]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-item.html) object at the specified index.

```cpp
virtual const CCapturedResultItem* operator[](int index) const = 0;
```

**Parameters**

`[in] index` The index of the item to retrieve.

**Return value**

Returns a pointer to the CCapturedResultItem object at the specified index.

### Retain

Increases the reference count of the `CCapturedResult` object.

```cpp
virtual CCapturedResultItem* Retain() = 0;
```

**Return value**

Return an object of `CCapturedResult`.

### Release

Decreases the reference count of the `CCapturedResult` object.

```cpp
virtual void Release() = 0;
```

### GetDecodedBarcodesResult

Gets the decoded barcode items from the `CCapturedResult`.

```cpp
dbr::CDecodedBarcodesResult* GetDecodedBarcodesResult() const
```

**Return value**

Returns a pointer to the CDecodedBarcodesResult object containing the decoded barcode items. 

**Remarks**

Do not forget to release the memory pointed to by the returned pointer.

### GetRecognizedTextLinesResult

Gets the recognized text line items from the `CCapturedResult`.

```cpp
dlr::CRecognizedTextLinesResult* GetRecognizedTextLinesResult() const
```

**Return value**

Returns a pointer to the CRecognizedTextLinesResult object containing the recognized text line items.

**Remarks**

Do not forget to release the memory pointed to by the returned pointer.

### GetDetectedQuadsResult

Gets the detected quads items from the `CCapturedResult`.

```cpp
ddn::CDetectedQuadsResult* GetDetectedQuadsResult() const
```

**Return value**

Returns a pointer to the CDetectedQuadsResult object containing the detected quads items.

**Remarks**

Do not forget to release the memory pointed to by the returned pointer.

### GetNormalizedImagesResult

Gets the normalized images items from the `CCapturedResult`.

```cpp
ddn::CNormalizedImagesResult* GetNormalizedImagesResult() const
```

**Return value**

Returns a pointer to the CNormalizedImagesResult object containing the normalized images items.

**Remarks**

Do not forget to release the memory pointed to by the returned pointer.

### GetParsedResult

Gets the parsed result items from the `CCapturedResult`.

```cpp
dpr::CParsedResult* GetParsedResult() const
```

**Return value**

Returns a pointer to the CParsedResult object containing the parsed result items.

**Remarks**

Do not forget to release the memory pointed to by the returned pointer.