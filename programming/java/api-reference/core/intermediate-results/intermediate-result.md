---
layout: default-layout
title: class IntermediateResult - Dynamsoft Core Module Java Edition API Reference
description: This page shows the java edition of the class IntermediateResult in Dynamsoft Core Module.
keywords: task results, intermediate results, java
needAutoGenerateSidebar: true
---

# IntermediateResult

The `IntermediateResult` class represents a container containing a collection of `IntermediateResultUnit` objects.

## Definition

*Package:* com.dynamsoft.core.intermediate_results

```java
public class IntermediateResult
```

## Methods

| Method | Description |
|--------|-------------|
| [`getCount`](#getcount) | Gets the count of `IntermediateResultUnit` objects in the collection. |
| [`getIntermediateResultUnit`](#getintermediateresultunit) | Gets the `IntermediateResultUnit` object at the specified index. |
| [`getIntermediateResultUnits`](#getintermediateresultunits) | Gets all `IntermediateResultUnit` objects in the collection. |

### getCount

Gets the count of `IntermediateResultUnit` objects in the collection.

```java
public int getCount()
```

**Return value**

Returns the count of `IntermediateResultUnit` objects in the collection.

### getIntermediateResultUnit

Gets the `IntermediateResultUnit` object at the specified index.

```java
public IntermediateResultUnit getIntermediateResultUnit(int index)
```

**Parameters**

`index` The index of the `IntermediateResultUnit` object to retrieve.

**Return value**

Returns the `IntermediateResultUnit` object at the specified index.

**See Also**

[IntermediateResultUnit]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-unit.html)

### getIntermediateResultUnits

Gets all `IntermediateResultUnit` objects in the collection.

```java
public IntermediateResultUnit[] getIntermediateResultUnits()
```

**Return value**

Returns all `IntermediateResultUnit` objects in the collection.

**See Also**

[IntermediateResultUnit]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-unit.html)
