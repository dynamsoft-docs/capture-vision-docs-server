---
layout: default-layout
title: class AbstractIntermediateResultReceiver - Dynamsoft Core Module Python Edition API Reference
description: This page shows the python edition of the class AbstractIntermediateResultReceiver in Dynamsoft Core Module.
keywords: abstractintermediate result receiver, python
needAutoGenerateSidebar: true
---

# AbstractIntermediateResultReceiver

The `AbstractIntermediateResultReceiver` class is responsible for receiving intermediate results of different types. It provides virtual functions for each type of result, which are called when the corresponding result is received.

## Definition

*Module:* dynamsoft_core

```python
class AbstractIntermediateResultReceiver(ABC)
```

## Methods

| Method | Description |
|--------|-------------|
| [`get_observation_parameters`](#get_observation_parameters) | Gets the observation parameters of the intermediate result receiver. |
| [`on_task_results_received`](#on_task_results_received) | Called when a task result has been received. |
| [`on_unit_result_received`](#on_unit_result_received) | Called when a intermediate result unit has been received. |


### get_observation_parameters

Gets the observation parameters of the intermediate result receiver.

```python
def get_observation_parameters(self) -> ObservationParameters:
```

**Return value**

Returns an `ObservationParameters` object. The default parameters are to observe all intermediate result unit types and all tasks.

**See Also**

[ObservationParameters]({{ site.dcvb_python_api }}core/intermediate-results/observed-parameters.html)

### on_task_results_received

Called when a task result has been received.

```python
@abstractmethod
def on_task_results_received(self, result: IntermediateResult, info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` An `IntermediateResult` object that contains several result units.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[IntermediateResult]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_unit_result_received

Called when a intermediate result unit has been received.

```python
@abstractmethod
def on_unit_result_received(self, unit: IntermediateResultUnit, info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`unit` An `IntermediateResultUnit` object.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[IntermediateResultUnit]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)
