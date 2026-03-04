---
layout: default-layout
title: CapturedResultArray Class - Dynamsoft Capture Vision Module Python Edition API Reference
description: API reference for the CapturedResultArray class in Dynamsoft Capture Vision Python Edition, which holds an array of captured results from batch processing.
keywords: captured result, python
needAutoGenerateSidebar: true
---

# CapturedResultArray

The `CapturedResultArray` class represents a collection of `CaptureResult`, each derived from a capture operation on an image. Internally, `CaptureResult` maintains an array of items, which may include barcodes, text lines, detected quads, normalized images, raw images, parsed items, and more.

## Definition

*Module:* cvr

```python
class CapturedResultArray
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_results`](#get_results) | Gets all `CapturedResult` objects from current result collection. |

### get_results

Gets all `CapturedResult` objects from current result collection.

```python
def get_results(self) -> List[CapturedResult]:
```

**Return value**

Returns a `CapturedResult` list.

**See Also**

[CapturedResult]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/captured-result.html)

