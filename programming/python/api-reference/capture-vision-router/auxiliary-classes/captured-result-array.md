---
layout: default-layout
title: CapturedResultArray Class - Dynamsoft Capture Vision Module Python Edition API Reference
description: Definition of CapturedResultArray class in Dynamsoft Capture Vision Module Python Edition.
keywords: captured result, python
needAutoGenerateSidebar: true
---

# CapturedResultArray

The `CapturedResultArray` class represents a collection of `CaptureResult`, each derived from a capture operation on an image. Internally, `CaptureResult` maintains an array of items, which may include barcodes, text lines, detected quads, normalized images, raw images, parsed items, and more.

## Definition

*Module:* dynamsoft_capture_vision_router

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

