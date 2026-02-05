---
layout: default-layout
title: class PredetectedRegionsUnit - Dynamsoft Core Module Java Edition API Reference
description: This page shows the Java edition of the class PredetectedRegionsUnit in Dynamsoft Core Module.
keywords: predetected regions, java
needAutoGenerateSidebar: true
---

# PredetectedRegionsUnit

The `PredetectedRegionsUnit` class represents a unit that contains a collection of pre-detected regions. It inherits from the `IntermediateResultUnit` class and stores the result of image color pre-detection.

## Definition

*Package:* com.dynamsoft.core.intermediate_results

```java
public class PredetectedRegionsUnit extends IntermediateResultUnit
```

## Methods

| Method | Description |
|--------|-------------|
| [`getCount`](#getcount) | Gets the number of pre-detected regions in the collection. |
| [`getPredetectedRegion`](#getpredetectedregion) | Gets a specific pre-detected region in the collection. |
| [`getPredetectedRegions`](#getpredetectedregions) | Gets all pre-detected regions in the collection. |
| [`removeAllPredetectedRegions`](#removeallpredetectedregions) | Removes all pre-detected regions in the unit. |
| [`removePredetectedRegion`](#removepredetectedregion) | Removes a pre-detected region in the unit at the specified index. |
| [`addPredetectedRegion`](#addpredetectedregion) | Adds a pre-detected region in the unit. |
| [`setPredetectedRegion`](#setpredetectedregion) | Sets a pre-detected region in the unit at the specified index. |

### getCount

Gets the number of pre-detected regions in the collection.

```java
int getCount()
```

**Return value**

Returns the number of pre-detected regions in the collection.

### getPredetectedRegion

Gets a specific pre-detected region in the collection.

```java
PredetectedRegionElement getPredetectedRegion(int index)
```

**Parameters**

`index` The index of the pre-detected region to retrieve.

**Return value**

Returns the specified pre-detected region in the collection.

**See Also**

[PredetectedRegionElement]({{ site.dcvb_java_api }}core/intermediate-results/predetected-region-element.html)

### getPredetectedRegions

Gets all pre-detected regions in the collection.

```java
PredetectedRegionElement[] getPredetectedRegions()
```

**Return value**

Returns all pre-detected regions in the collection.

**See Also**

[PredetectedRegionElement]({{ site.dcvb_java_api }}core/intermediate-results/predetected-region-element.html)

### removeAllPredetectedRegions

Removes all pre-detected regions in the unit.

```java
void removeAllPredetectedRegions()
```

### removePredetectedRegion

Removes a pre-detected region in the unit at the specified index.

```java
void removePredetectedRegion(int index) throws CoreException
```

**Parameters**

`index` The index of the pre-detected region to remove.

**Exception**

[CoreException]({{ site.dcvb_java_api }}core/basic-classes/core-exception.html)

### addPredetectedRegion

Adds a pre-detected region in the unit.

```java
void addPredetectedRegion(PredetectedRegionElement element) throws CoreException
void addPredetectedRegion(PredetectedRegionElement element, double[] matrixToOriginalImage) throws CoreException
```

**Parameters**

`element` The pre-detected region to add.

`matrixToOriginalImage` The transform matrix to the original image.

**Exception**

[CoreException]({{ site.dcvb_java_api }}core/basic-classes/core-exception.html)

**See Also**

[PredetectedRegionElement]({{ site.dcvb_java_api }}core/intermediate-results/predetected-region-element.html)

### setPredetectedRegion

Sets a pre-detected region in the unit at the specified index.

```java
void setPredetectedRegion(int index, PredetectedRegionElement element) throws CoreException
void setPredetectedRegion(int index, PredetectedRegionElement element, double[] matrixToOriginalImage) throws CoreException
```

**Parameters** 

`index` The index of the pre-detected region to set.

`element` The pre-detected region to set.

`matrixToOriginalImage` The transform matrix to the original image.

**Exception**

[CoreException]({{ site.dcvb_java_api }}core/basic-classes/core-exception.html)

**See Also**

[PredetectedRegionElement]({{ site.dcvb_java_api }}core/intermediate-results/predetected-region-element.html)
