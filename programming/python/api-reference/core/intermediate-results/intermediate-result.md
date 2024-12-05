---
layout: default-layout
title: class IntermediateResult - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class IntermediateResult in Dynamsoft Core Module.
keywords: task results, intermediate results, python
needAutoGenerateSidebar: true
---

# IntermediateResult

The `IntermediateResult` class represents a container containing a collection of `IntermediateResultUnit` objects.

## Definition

*Module:* dynamsoft_core

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
