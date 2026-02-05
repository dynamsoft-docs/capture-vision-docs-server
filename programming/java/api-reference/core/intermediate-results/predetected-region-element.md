---
layout: default-layout
title: class PredetectedRegionElement - Dynamsoft Core Module Java Edition API Reference
description: This page shows the Java edition of the class PredetectedRegionElement in Dynamsoft Core Module.
keywords: predetected region element, java
---

# PredetectedRegionElement

The `PredetectedRegionElement` class represents a region element that has been pre-detected in an image. It is a subclass of the `RegionObjectElement`.

## Definition

*Package:* com.dynamsoft.core.intermediate_results

```java
public class PredetectedRegionElement extends RegionObjectElement
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`PredetectedRegionElement`](#predetectedregionelement) | Initializes a new instance of the `PredetectedRegionElement` class. |
| [`getModeName`](#getmodename) | Gets the name of the detection mode used to detect this region element. |
| [`setLocation`](#setlocation)   | Sets the location of the region object element. |
| [`getLabelId`](#getlabelid)     | Gets the label id of the region object element. |
| [`getLabelName`](#getlabelname) | Gets the label name of the region object element. |

### PredetectedRegionElement

Initializes a new instance of the `PredetectedRegionElement` class.

```java
PredetectedRegionElement()
```

### getModeName

Gets the name of the detection mode used to detect this region element.

```java
String getModeName()
```

**Return value**

Returns the name of the detection mode used to detect this region element.

### setLocation

Set the location of the region object element.

```java
void setLocation(Quadrilateral location) throws CoreException
```

**Parameters**

`location` The location of the region object element.

**Exception**

[CoreException]({{ site.dcvb_java_api }}core/basic-classes/core-exception.html)

**See Also**

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

### getLabelId

Gets the label id of the predetected region element.

```java
int getLabelId()
```

**Return value**

Returns the label id of the predetected region element.

### getLabelName

Gets the label name of the predetected region element.

```java
String getLabelName()
```

**Return value**

Returns the label name of the predetected region element.