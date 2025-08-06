---
layout: default-layout
title: class AbstractIntermediateResultReceiver - Dynamsoft Core Module Java Edition API Reference
description: This page shows the java edition of the class AbstractIntermediateResultReceiver in Dynamsoft Core Module.
keywords: abstractintermediate result receiver, java
needAutoGenerateSidebar: true
---

# AbstractIntermediateResultReceiver

The `AbstractIntermediateResultReceiver` class is responsible for receiving intermediate results of different types. It provides virtual functions for each type of result, which are called when the corresponding result is received.

## Definition

*Package:* `com.dynamsoft.core.intermediate_results`

```java
public abstract class AbstractIntermediateResultReceiver
```

## Methods

| Method | Description |
|--------|-------------|
| [`getObservationParameters`](#getobservationparameters) | Gets the observation parameters of the intermediate result receiver. |
| [`onTaskResultsReceived`](#ontaskresultsreceived) | Called when a task result has been received. |
| [`onUnitResultReceived`](#onunitresultreceived) | Called when a intermediate result unit has been received. |


### getObservationParameters

Gets the observation parameters of the intermediate result receiver.

```java
ObservationParameters getObservationParameters()
```

**Return value**

Returns an `ObservationParameters` object. The default parameters are to observe all intermediate result unit types and all tasks.

**See Also**

[ObservationParameters]({{ site.dcvb_java_api }}core/intermediate-results/observed-parameters.html)

### onTaskResultsReceived

Called when a task result has been received.

```java
public abstract void onTaskResultsReceived(IntermediateResult result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` An `IntermediateResult` object that contains several result units.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[IntermediateResult]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onUnitResultReceived

Called when a intermediate result unit has been received.

```java
public abstract void onUnitResultReceived(IntermediateResultUnit unit, IntermediateResultExtraInfo info)
```

**Parameters**

`unit` An `IntermediateResultUnit` object.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[IntermediateResultUnit]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)
