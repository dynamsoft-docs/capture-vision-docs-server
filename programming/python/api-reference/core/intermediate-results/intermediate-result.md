---
layout: default-layout
title: class IntermediateResult - Dynamsoft Core Module Python Edition API Reference
description: API reference for the IntermediateResult class in Dynamsoft Core Module Python Edition, which contains a collection of intermediate result units from one stage of image processing.
keywords: task results, intermediate results, python
needAutoGenerateSidebar: true
---

# IntermediateResult

The `IntermediateResult` class represents a container containing a collection of `IntermediateResultUnit` objects.

## Definition

*Module:* core

```python
class IntermediateResult
```

## Methods

| Method | Description |
|--------|-------------|
| [`get_intermediate_result_units`](#get_intermediate_result_units) | Gets all `IntermediateResultUnit` objects in the collection. |

### get_intermediate_result_units

Gets all `IntermediateResultUnit` objects in the collection.

```python
def get_intermediate_result_units(self) -> List[IntermediateResultUnit]:
```

**Return value**

Returns all `IntermediateResultUnit` objects in the collection.

**See Also**

[IntermediateResultUnit]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-unit.html)
