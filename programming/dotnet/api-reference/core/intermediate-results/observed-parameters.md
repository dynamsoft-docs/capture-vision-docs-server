---
layout: default-layout
title: class ObservationParameters - Dynamsoft Core Module .NET Edition API Reference
description: This page shows the .NET Edition of the class ObservationParameters in Dynamsoft Core Module.
keywords: intermediate result, .NET
needAutoGenerateSidebar: true
---

# ObservationParameters

The `ObservationParameters` class is used to set filter conditions for the `IntermediateResultReceiver`, so that only intermediate results meeting specific conditions will be called back.

## Definition

*Namespace:* Dynamsoft.Core.intermediate_results


```csharp
public class ObservationParameters : IDisposable
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`SetObservedResultUnitTypes`](#setobservedresultunittypes) | Sets the types of intermediate result units that have been observed.|
| [`GetObservedResultUnitTypes`](#getobservedresultunittypes) | Gets the types of intermediate result units that have been observed. |
| [`IsResultUnitTypeObserved`](#isresultunittypeobserved) | Determines whether the specified result unit type was observed. |
| [`AddObservedTask`](#addobservedtask) | Adds observed task name to be notified when relevant results are available. |
| [`RemoveObservedTask`](#removeobservedtask) | Remove the observed task name so that intermediate results generated by the task are not notified. |
| [`IsTaskObserved`](#istaskobserved) | Determines whether the specified task was observed. |
| [`SetResultUnitTypesOnlyForInput`](#setresultunittypesonlyforinput) | Sets the type of intermediate result unit that indicates skipping default calculations and replacing with input data units. |
| [`GetResultUnitTypesOnlyForInput`](#getresultunittypesonlyforinput) | Gets the type of intermediate result unit that indicates skipping default calculations and replacing with input data units. |
| [`IsResultUnitTypeOnlyForInput`](#isresultunittypeonlyforinput) | Determines whether the specified type of intermediate result unit indicates skipping default calculations and replacing with input data units. |

### SetObservedResultUnitTypes

Sets the types of intermediate result units that have been observed.

```csharp
void SetObservedResultUnitTypes(ulong types)
```

**Parameters**

`[in] types` The observed types of intermediate result units.

**See Also**

[EnumIntermediateResultUnitType]({{ site.dcvb_dotnet_api }}core/enum-intermediate-result-unit-type.html)

### GetObservedResultUnitTypes

Gets the types of intermediate result units that have been observed.

```csharp
ulong GetObservedResultUnitTypes()
```

**Return value**

The observed types of intermediate result units.

**See Also**

[EnumIntermediateResultUnitType]({{ site.dcvb_dotnet_api }}core/enum-intermediate-result-unit-type.html)

### IsResultUnitTypeObserved

Determines whether the specified result unit type was observed.

```csharp
bool IsResultUnitTypeObserved(EnumIntermediateResultUnitType type)
```

**Parameters**

`[in] type` The result unit type to check.

**Return value**

Returns a boolean value indicating whether the specified result unit type was observed.

**See Also**

[EnumIntermediateResultUnitType]({{ site.dcvb_dotnet_api }}core/enum-intermediate-result-unit-type.html)

### AddObservedTask

Adds observed task name to be notified when relevant results are available.

```csharp
void AddObservedTask(string taskName)
```

**Parameters**

`[in] taskName` The specified task name.

### RemoveObservedTask

Remove the observed task name so that intermediate results generated by the task are not notified.

```csharp
void RemoveObservedTask(string taskName)
```

**Parameters**

`[in] taskName` The specified task name.

### IsTaskObserved

Determines whether the specified task was observed.

```csharp
bool IsTaskObserved(string taskName)
```

**Parameters**

`[in] taskName` The specified task name.

**Return value**

Returns a boolean value indicating whether the specified task was observed.

### SetResultUnitTypesOnlyForInput

Sets the type of intermediate result unit that indicates skipping default calculations and replacing with input data units.

```csharp
void SetResultUnitTypesOnlyForInput(ulong types)
```

**Parameters**

`types`: The type of intermediate result unit that serves as the combination value of `EnumIntermediateResultUnitType`.

**See Also**

[EnumIntermediateResultUnitType]({{ site.dcvb_dotnet_api }}core/enum-intermediate-result-unit-type.html)

### GetResultUnitTypesOnlyForInput

Gets the type of intermediate result unit that indicates skipping default calculations and replacing with input data units.

```csharp
ulong GetResultUnitTypesOnlyForInput()
```

**Return**

Returns the type of intermediate result unit that serves as the combination value of `EnumIntermediateResultUnitType`.

**See Also**

[EnumIntermediateResultUnitType]({{ site.dcvb_dotnet_api }}core/enum-intermediate-result-unit-type.html)

### IsResultUnitTypeOnlyForInput

Determines whether the specified type of intermediate result unit indicates skipping default calculations and replacing with input data units.

```csharp
bool IsResultUnitTypeOnlyForInput(EnumIntermediateResultUnitType type)
```

**Parameters**

`type`: The type of intermediate result unit to check.

**Return**

Returns a boolean value indicating whether the specified type of intermediate result unit indicates skipping default calculations and replacing with input data units.

**See Also**

[EnumIntermediateResultUnitType]({{ site.dcvb_dotnet_api }}core/enum-intermediate-result-unit-type.html)
