---
layout: default-layout
title: class CCapturedResult - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CCapturedResult in Dynamsoft Core Module.
keywords: captured result, c++
needAutoGenerateSidebar: true
---

# CCapturedResult

The CCapturedResult class represents the result of a capture operation on an image. Internally, CaptureResult stores an array that contains multiple items, each of which may be a barcode, text line, detected quad, normalized image, raw image, parsed item, etc.

```cpp
class dynamsoft::core::basic_structures::CCapturedResult 
```

---

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetSourceImageHashId`](#getsourceimagehashid) | It is used to get the hash ID of the source image.|
| [`GetSourceImageTag`](#getsourceimagetag) | It is used to get the tag of the source image.|
| [`GetCount`](#getcount) | It is used to get the number of items in the captured result.|
| [`GetItem`](#getitem) | It is used to get a specific item in the captured result.|
| [`GetErrorCode`](#geterrorcode) | It is used to get the error code of the capture operation.|
| [`GetErrorString`](#geterrorstring) | It is used to get the error message of the capture operation.|

### GetSourceImageHashId

It is used to get the hash ID of the source image.

```cpp
const char* GetSourceImageHashId() const
```

**Return value**

Returns the hash ID of the source image as a null-terminated string. You are not required to release the memory pointed to by the returned pointer.

### GetSourceImageTag

It is used to get the tag of the source image.

```cpp
const CImageTag* GetSourceImageTag() const
```

**Return value**

Returns a pointer to the CImageTag object containing the tag of the source image. You are not required to release the memory pointed to by the returned pointer.

### GetCount

It is used to get the number of items in the captured result.

```cpp
int GetCount() const
```

**Return value**

Returns the number of items in the captured result.

### GetItem

It is used to get a specific item in the captured result.

```cpp
const CCapturedResultItem* GetItem(int index) const
```

**Parameters**

`[in] index` The index of the item to retrieve.

**Return value**

Returns a pointer to the CCapturedResultItem object at the specified index.

### GetErrorCode

It is used to get the error code of the capture operation.

```cpp
int GetErrorCode() const
```

**Return value**

Returns the error code of the capture operation.

### GetErrorString

It is used to get the error message of the capture operation.

```cpp
const char* GetErrorString() const
```

**Return value**

Returns the error message of the capture operation as a null-terminated string. You are not required to release the memory pointed to by the returned pointer.
