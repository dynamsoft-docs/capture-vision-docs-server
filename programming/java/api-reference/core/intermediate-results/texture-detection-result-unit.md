---
layout: default-layout
title: class TextureDetectionResultUnit - Dynamsoft Core Module Java Edition API Reference
description: This page shows the Java edition of the class TextureDetectionResultUnit in Dynamsoft Core Module.
keywords: texture detection result, java
needAutoGenerateSidebar: true
---

# TextureDetectionResultUnit

The `TextureDetectionResultUnit` class represents an intermediate result unit for texture detection. It is derived from the `IntermediateResultUnit` class and contains the x-direction spacing and y-direction spacing of the texture stripes.

## Definition

*Package:* com.dynamsoft.core.intermediate_results

```java
public class TextureDetectionResultUnit extends IntermediateResultUnit
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getXSpacing`](#getxspacing) | Gets x-direction spacing of the texture stripes. |
| [`getYSpacing`](#getyspacing) | Gets y-direction spacing of the texture stripes. |
| [`setXSpacing`](#setxspacing) | Sets x-direction spacing of the texture stripes. |
| [`setYSpacing`](#setyspacing) | Sets y-direction spacing of the texture stripes. |

### getXSpacing

Gets x-direction spacing of the texture stripes.

```java
int getXSpacing()
```

**Return value**

Returns the x-direction spacing of the texture stripes.

### getYSpacing

Gets y-direction spacing of the texture stripes.

```java
int getYSpacing()
```

**Return value**

Returns the y-direction spacing of the texture stripes.

### setXSpacing

Sets the x-direction spacing of the texture stripes.

```java
void setXSpacing(int xSpacing)
```

**Parameters**

`xSpacing` The x-direction spacing of the texture stripes.

### setYSpacing

Sets the y-direction spacing of the texture stripes.

```java
void setYSpacing(int ySpacing)
```

**Parameters**

`ySpacing` The y-direction spacing of the texture stripes.
