---
layout: default-layout
title: class IntermediateResult - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class IntermediateResult in Dynamsoft Core Module.
keywords: task results, intermediate results, .NET
needAutoGenerateSidebar: true
---

# IntermediateResult

The `IntermediateResult` class represents a container containing a collection of `IntermediateResultUnit` objects.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results


```csharp
class IntermediateResult : IEnumerable<IntermediateResultUnit>
```

## Methods

| Method | Description |
|--------|-------------|
| [`GetCount`](#getcount) | Gets the number of `IntermediateResultUnit` objects in the collection. |
| [`GetIntermediateResultUnit`](#getintermediateresultunit) | Gets a specific `IntermediateResultUnit` object in the collection. |
| [`GetIntermediateResultUnits`](#getintermediateresultunits) | Gets all `IntermediateResultUnit` objects in the collection. |

### GetCount

Gets the number of `IntermediateResultUnit` objects in the collection.

```csharp
int GetCount()
```

**Return value**

Returns the number of `IntermediateResultUnit` objects in the collection.

### GetIntermediateResultUnit

Gets a specific `IntermediateResultUnit` object in the collection.

```csharp
IntermediateResultUnit GetIntermediateResultUnit(int index)
```

**Parameters**

`[in] index` The index of the `IntermediateResultUnit` object to retrieve.

**Return value**

Returns the specified `IntermediateResultUnit` object in the collection.

**See Also**

[IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html)

### GetIntermediateResultUnits

Gets all `IntermediateResultUnit` objects in the collection.

```csharp
IntermediateResultUnit[] GetIntermediateResultUnits()
```

**Return value**

Returns all `IntermediateResultUnit` objects in the collection.

**See Also**

[IntermediateResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-unit.html)
