---
layout: default-layout
title: class Vector4 - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class Vector4 in Dynamsoft Core Module.
keywords: vector4, python
needAutoGenerateSidebar: true
---

# Vector4

The `Vector4` class represents a four-dimensional vector.

## Definition

*Module:* dynamsoft_core

```python
class Vector4
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `Vector4` class. |
| [`__getitem__`](#__getitem__) | Gets the component value at the specified index in the `Vector4`. |
| [`__setitem__`](#__setitem__) | Sets the components value of a four-dimensional vector. |

### \_\_init\_\_

Initializes a new instance of the `Vector4` class.

```python
def __init__(self):
```

### \_\_setitem\_\_

Sets the components value at the specified index in the `Vector4`.

```python
def __setitem__(self, index: int, value: int) -> None:
```

**Parameters**

`index` The index at which to set the value.

`value` The component value to assign at the specified index.

### \_\_getitem\_\_

Gets the component value at the specified index in the `Vector4`.

```python
def __getitem__(self, index: int) -> int:
```

**Parameters**

`index` An integer index used to access the component value of the `Vector4`.

**Return Value**

A reference to the component value at the specified index in the `Vector4`.
