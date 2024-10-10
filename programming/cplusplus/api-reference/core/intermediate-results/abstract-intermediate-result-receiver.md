---
layout: default-layout
title: class CAbstractIntermediateResultReceiver - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CAbstractIntermediateResultReceiver in Dynamsoft Core Module.
keywords: abstractintermediate result receiver, c++
needAutoGenerateSidebar: true
---

# CAbstractIntermediateResultReceiver

The `CAbstractIntermediateResultReceiver` class is responsible for receiving intermediate results of different types. It provides virtual functions for each type of result, which are called when the corresponding result is received.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore

```cpp
class CAbstractIntermediateResultReceiver 
```

## Methods Summary

| Method | Description |
|--------|-------------|
| [`GetObservationParameters`](#getobservationparameters) | Gets the observation parameters of the intermediate result receiver. |
| [`OnTaskResultsReceived`](#ontaskresultsreceived) | Called when a task result has been received. |
| [`OnUnitResultReceived`](#onunitresultreceived) | Called when a intermediate result unit has been received. |


### GetObservationParameters

Gets the observation parameters of the intermediate result receiver.

```cpp
CObservationParameters* GetObservationParameters()
```

**Return value**

Returns the object of `CObservationParameters`. The default parameters are to observe all intermediate result unit types and all tasks.

**See Also**

[CObservationParameters]({{ site.dcvb_cpp_api }}core/intermediate-results/observed-parameters.html)

### OnTaskResultsReceived

Called when a task result has been received.

```cpp
virtual void OnTaskResultsReceived(CIntermediateResult *pResult, const IntermediateResultExtraInfo* info) = 0
```

**Parameters**

`[in] pResult` A pointer to the `CIntermediateResult` object that contains several result units.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CIntermediateResult]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnUnitResultReceived

Called when a intermediate result unit has been received.

```cpp
virtual void OnUnitResultReceived(CIntermediateResultUnit *pUnit, const IntermediateResultExtraInfo* info) = 0;
```

**Parameters**

`[in] pUnit` A pointer to the `CIntermediateResultUnit` object.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CIntermediateResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)
