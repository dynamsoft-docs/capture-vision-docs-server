---
layout: default-layout
title: class IntermediateResultExtraInfo - Dynamsoft Core Module Java Edition API Reference
description: This page shows the Java edition of the class IntermediateResultExtraInfo in Dynamsoft Core Module.
keywords: intermediate result, java
needAutoGenerateSidebar: true
---

# IntermediateResultExtraInfo

The `IntermediateResultExtraInfo` class represents the extra information for generating an intermediate result unit.

## Definition

*Namespace:* com.dynamsoft.core

```java
public class IntermediateResultExtraInfo
```

## Attributes

| Attribute                                             | Type    | Description |
| ----------------------------------------------------- | ------- | ----------- |
| [`targetROIDefName`](#targetroidefname)         | *String*   | Specifies the name of the `TargetROIDef` object that generates the intermediate result. |
| [`taskName`](#taskname)                             | *String*   | Specifies the name of the task that generates the intermediate result. |
| [`isSectionLevelResult`](#issectionlevelresult) | *boolean*  | Specifies whether the intermediate result is section-level result. |
| [`sectionType`](#sectiontype)                       | *int*   | Specifies the section type that generates the intermediate result. This is one of the values of the [EnumSectionType]({{ site.dcvb_java_api }}core/enum-section-type.html) enumeration. |

### targetROIDefName

Specifies the name of the `TargetROIDef` object that generates the intermediate result.

```java
String targetROIDefName
```

### taskName

Specifies the name of the task that generates the intermediate result.

```java
String taskName
```

### isSectionLevelResult

Specifies whether the intermediate result is section-level result.

```java
boolean isSectionLevelResult
```

### sectionType

Specifies the section type that generates the intermediate result.

```java
@EnumSectionType int sectionType
```

**See Also**

[EnumSectionType]({{ site.dcvb_java_api }}core/enum-section-type.html)
