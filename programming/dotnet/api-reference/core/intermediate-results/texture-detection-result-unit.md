---
layout: default-layout
title: class TextureDetectionResultUnit - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class TextureDetectionResultUnit in Dynamsoft Core Module.
keywords: texture detection result, .NET
needAutoGenerateSidebar: true
---

# TextureDetectionResultUnit

The `TextureDetectionResultUnit` class represents an intermediate result unit for texture detection. It is derived from the `IntermediateResultUnit` class and contains the x-direction spacing and y-direction spacing of the texture stripes.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results


```csharp
class TextureDetectionResultUnit : IntermediateResultUnit 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetXSpacing`](#getxspacing) | Gets x-direction spacing of the texture stripes. |
| [`GetYSpacing`](#getyspacing) | Gets y-direction spacing of the texture stripes. |
| [`SetXSpacing`](#setxspacing) | Sets x-direction spacing of the texture stripes. |
| [`SetYSpacing`](#setyspacing) | Sets y-direction spacing of the texture stripes. |

### Inherited Methods

Checkout inherited methods from [IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html) for more details.

### GetXSpacing

Gets x-direction spacing of the texture stripes.

```csharp
int GetXSpacing() 
```

**Return value**

Returns the x-direction spacing of the texture stripes.

### GetYSpacing

Gets y-direction spacing of the texture stripes.

```csharp
int GetYSpacing() 
```

**Return value**

Returns the y-direction spacing of the texture stripes.

### SetXSpacing

Sets the x-direction spacing of the texture stripes.

```csharp
void SetXSpacing(int xSpacing)
```

**Parameters**

`[in] xSpacing` The x-direction spacing of the texture stripes.

### SetYSpacing

Sets the y-direction spacing of the texture stripes.

```csharp
void SetYSpacing(int ySpacing)
```

**Parameters**

`[in] ySpacing` The y-direction spacing of the texture stripes.
