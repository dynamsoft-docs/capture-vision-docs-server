---
layout: default-layout
title: class TextZonesUnit - Dynamsoft Core Module Java Edition API Reference
description: This page shows the Java edition of the class TextZonesUnit in Dynamsoft Core Module.
keywords: text zones, java
needAutoGenerateSidebar: true
---

# TextZonesUnit

The `TextZonesUnit` class represents a unit that contains text zones. It is derived from `IntermediateResultUnit` class and provides methods to retrieve the count and details of text zones.

## Definition

*Package:* com.dynamsoft.core.intermediate_results

```java
public class TextZonesUnit extends IntermediateResultUnit
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getCount`](#getcount) | Gets the number of text zones.|
| [`getTextZone`](#gettextzone) | Gets the text zone at the specified index. |
| [`getTextZones`](#gettextzones) | Gets all text zones. |
| [`removeAllTextZones`](#removealltextzones) | Removes all text zones from the unit. |
| [`removeTextZone`](#removetextzone) | Removes the text zone at the specified index. |
| [`addTextZone`](#addtextzone) | Adds a text zone to the unit. |
| [`setTextZone`](#settextzone) | Sets the text zone at the specified index. |

### getCount

Gets the number of text zones in the unit.

```java
int getCount()
```

**Return value**

Returns the number of text zones in the unit.

### getTextZone

Gets the text zone at the specified index.

```java
TextZone getTextZone(int index) throws CoreException
```

**Parameters**

`index` The index of the text zone.

**Return Value**

Returns the `TextZone` object at the specified index.

**Exception**

[`CoreException`]({{ site.dcvb_java_api }}core/core-exception.html)

**See Also**

[TextZone]({{ site.dcvb_java_api }}core/intermediate-results/text-zone.html)

### getTextZones

Gets all text zones.

```java
TextZone[] getTextZones()
```

**Return Value**

Returns an array of `TextZone` objects representing all text zones.

**See Also**

[TextZone]({{ site.dcvb_java_api }}core/intermediate-results/text-zone.html)

### removeAllTextZones

Removes all text zones from the unit.

```java
void removeAllTextZones()
```

### removeTextZone

Removes the text zone at the specified index.

```java
void removeTextZone(int index) throws CoreException
```

**Parameters**

`index` The index of the text zone to remove.

**Exception**

[`CoreException`]({{ site.dcvb_java_api }}core/core-exception.html)

### addTextZone

Adds a text zone to the unit.

```java
void addTextZone(TextZone textZone) throws CoreException
void addTextZone(TextZone textZone, double[] matrixToOriginalImage) throws CoreException
```

**Parameters**

`textZone` The text zone to add.

`matrixToOriginalImage` The transform matrix to original image. The array length must be 9.

**Exception**

[`CoreException`]({{ site.dcvb_java_api }}core/core-exception.html)

**See Also**

[TextZone]({{ site.dcvb_java_api }}core/intermediate-results/text-zone.html)

### setTextZone

Sets the text zone at the specified index.

```java
void setTextZone(int index, TextZone textZone) throws CoreException
void setTextZone(int index, TextZone textZone, double[] matrixToOriginalImage) throws CoreException
```

**Parameters**

`index` The index of the text zone to set.

`textZone` The text zone to set.

`matrixToOriginalImage` The transform matrix to original image. The array length must be 9.

**Exception**

[`CoreException`]({{ site.dcvb_java_api }}core/core-exception.html)

**See Also**

[TextZone]({{ site.dcvb_java_api }}core/intermediate-results/text-zone.html)

