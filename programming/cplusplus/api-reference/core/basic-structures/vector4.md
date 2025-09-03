---
layout: default-layout
title: class CVector4 - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CVector4 in Dynamsoft Core Module.
keywords: vector4, c++
needAutoGenerateSidebar: true
---

# CVector4

The `CVector4` class represents a four-dimensional vector.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore

```cpp
class CVector4;
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`Set`](#set) | Sets the components value of a four-dimensional vector. |
| [`operator[]`](#operator) | Gets the component value at the specified index in the `CVector4`. |

### Set

Sets the components value of a four-dimensional vector.

```cpp
void Set(int v1, int v2, int v3, int v4)
```

**Parameters**

`[in] v1` The first component value of the four-dimensional vector.

`[in] v2` The second component value of the four-dimensional vector.

`[in] v3` The third component value of the four-dimensional vector.

`[in] v4` The fourth component value of the four-dimensional vector.

### operator[]

Gets the component value at the specified index in the `CVector4`.

```cpp
int& operator[](int i)
```

**Parameters**

`[in] i` An integer index used to access the component value of the `CVector4`.

**Return Value**

A reference to the component value at the specified index in the `CVector4`.
