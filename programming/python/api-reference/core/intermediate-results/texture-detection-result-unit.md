---
layout: default-layout
title: class TextureDetectionResultUnit - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class TextureDetectionResultUnit in Dynamsoft Core Module.
keywords: texture detection result, python
needAutoGenerateSidebar: true
---

# TextureDetectionResultUnit

The `TextureDetectionResultUnit` class represents an intermediate result unit for texture detection. It is derived from the `IntermediateResultUnit` class and contains the x-direction spacing and y-direction spacing of the texture stripes.

## Definition

*Module:* dynamsoft_core

```python
class TextureDetectionResultUnit(IntermediateResultUnit)
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_x_spacing`](#get_x_spacing) | Gets x-direction spacing of the texture stripes. |
| [`get_y_spacing`](#get_y_spacing) | Gets y-direction spacing of the texture stripes. |
| [`set_x_spacing`](#set_x_spacing) | Sets x-direction spacing of the texture stripes. |
| [`set_y_spacing`](#set_y_spacing) | Sets y-direction spacing of the texture stripes. |

### get_x_spacing

Gets x-direction spacing of the texture stripes.

```python
def get_x_spacing(self) -> int: 
```

**Return value**

Returns the x-direction spacing of the texture stripes.

### get_y_spacing

Gets y-direction spacing of the texture stripes.

```python
def get_y_spacing(self) -> int: 
```

**Return value**

Returns the y-direction spacing of the texture stripes.

### set_x_spacing

Sets the x-direction spacing of the texture stripes.

```python
def set_x_spacing(self, x_spacing: int) -> None:
```

**Parameters**

`x_spacing` The x-direction spacing of the texture stripes.

### set_y_spacing

Sets the y-direction spacing of the texture stripes.

```python
def set_y_spacing(self, y_spacing: int) -> None:
```

**Parameters**

`y_spacing` The y-direction spacing of the texture stripes.
