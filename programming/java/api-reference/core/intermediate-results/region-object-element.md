---
layout: default-layout
title: class RegionObjectElement - Dynamsoft Core Module Java Edition API Reference
description: This page shows the Java edition of the class RegionObjectElement in Dynamsoft Core Module.
keywords: region object element, java
needAutoGenerateSidebar: true
---

# RegionObjectElement

The `RegionObjectElement` class represents an element of a region object in 2D space. It is an abstract class that provides the interface for region object elements.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

```java
public class RegionObjectElement
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getLocation`](#getlocation) | Gets the location of the region object element. |
| [`getReferenceElement`](#getreferenceelement) | Gets a referenced region object element. |
| [`getElementType`](#getelementtype) | Gets the type of the region object element. |
| [`getImageData`](#getimagedata) | Get the imageData of the region object element. |
| [`clone`](#clone) | Clones the region object element. |

### getLocation

Gets the location of the region object element.

```java
Quadrilateral getLocation()
```

**Return value**

Returns a `Quadrilateral` object which represents the location of the region object element.

**See Also**

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

### getReferenceElement

Gets a referenced region object element.

```java
RegionObjectElement getReferenceElement()
```

**Return value**

Returns a referenced `RegionObjectElement` object.

**See Also**

[RegionObjectElement]({{ site.dcvb_java_api }}core/intermediate-results/region-object-element.html)

### getElementType

Gets the type of the region object element.

```java
@EnumRegionObjectElementType int getElementType()
```

**Return value**

Returns a `EnumRegionObjectElementType` enum value which represents the type of the region object element.

**See Also**

[EnumRegionObjectElementType]({{ site.dcvb_java_api }}core/enum-region-object-element-type.html)

### getImageData

Get the imageData of the region object element.

```java
ImageData getImageData()
```

**Return value**

Returns an `ImageData` object that contains the image data of current object.

**See Also**

[ImageData]({{ site.dcvb_java_api }}core/basic-classes/image-data.html)

### clone

Clones the region object element.

```java
RegionObjectElement clone()
```

**Return value**

Returns a copy of the region object element.

