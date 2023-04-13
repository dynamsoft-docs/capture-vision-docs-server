---
layout: default-layout
title: class CCapturedResultArray - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CCapturedResultArray in Dynamsoft Core Module.
keywords: captured result array, c++
needAutoGenerateSidebar: true
---

# CCapturedResultArray

The CCapturedResultArray class represents an array of captured results.

```cpp
class dynamsoft::core::basic_structures::CCapturedResultArray 
```

---

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetCount`](#getcount) | It is used to get the count of captured results.|
| [`GetResult`](#getresult) | It is used to get a specific captured result at a given index. |

### GetCount

It is used to get the count of captured results.

```cpp
virtual int GetCount() const
```

**Return value**

Returns the count of captured results.

### GetResult

It is used to get a specific captured result at a given index.

```cpp
virtual const CCapturedResult* GetResult(int index) const
```

**Parameters**

`[in] index` The index of the result to get.

**Return value**

Returns a pointer to the CCapturedResult object at the given index. You are not required to release the memory pointed to by the returned pointer.