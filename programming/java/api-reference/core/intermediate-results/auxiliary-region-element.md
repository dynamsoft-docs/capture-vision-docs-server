---
layout: default-layout
title: class AuxiliaryRegionElement - Dynamsoft Core Module Java Edition API Reference
description: This page shows the Java edition of the class AuxiliaryRegionElement in Dynamsoft Core Module.
keywords: auxiliary region element, java
---

# AuxiliaryRegionElement

The `AuxiliaryRegionElement` class represents an auxiliary region element that contains additional region information detected during processing (e.g., MRZ, portrait zones, signature areas). It inherits from the `RegionObjectElement` class.

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

## Definition

*Package:* com.dynamsoft.core.intermediate_results

*Inheritance:* [RegionObjectElement]({{ site.dcvb_java_api }}core/intermediate-results/region-object-element.html) -> AuxiliaryRegionElement

```java
public class AuxiliaryRegionElement extends RegionObjectElement
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`AuxiliaryRegionElement`](#auxiliaryregionelement) | Constructor. Initializes a new instance of the `AuxiliaryRegionElement` class. |
| [`getName`](#getname) | Gets the name of this auxiliary region. |
| [`getConfidence`](#getconfidence) | Gets the confidence level of this auxiliary region detection. |
| [`setName`](#setname) | Sets the name of this auxiliary region. |
| [`setLocation`](#setlocation) | Sets the location of this auxiliary region. |
| [`setConfidence`](#setconfidence) | Sets the confidence level of this auxiliary region detection. |
| **Methods Inherited from [RegionObjectElement]({{ site.dcvb_java_api }}core/intermediate-results/region-object-element.html):** | |
| [`getLocation`]({{ site.dcvb_java_api }}core/intermediate-results/region-object-element.html#getlocation) | Gets the location of the region object element. |
| [`getReferenceElement`]({{ site.dcvb_java_api }}core/intermediate-results/region-object-element.html#getreferenceelement) | Gets a referenced region object element. |
| [`getElementType`]({{ site.dcvb_java_api }}core/intermediate-results/region-object-element.html#getelementtype) | Gets the type of the region object element. |
| [`getImageData`]({{ site.dcvb_java_api }}core/intermediate-results/region-object-element.html#getimagedata) | Gets the imageData of the region object element. |
| [`clone`]({{ site.dcvb_java_api }}core/intermediate-results/region-object-element.html#clone) | Clones the region object element. |

### AuxiliaryRegionElement

Constructor. Initializes a new instance of the `AuxiliaryRegionElement` class.

```java
AuxiliaryRegionElement()
```

### getName

Gets the name of this auxiliary region.

```java
String getName()
```

**Return value**

Returns a string representing the region name (e.g., "MRZ", "PortraitZone", "SignatureArea").

### getConfidence

Gets the confidence level of this auxiliary region detection.

```java
int getConfidence()
```

**Return value**

Returns the confidence value, typically in the range [0, 100].

### setName

Sets the name of this auxiliary region.

```java
void setName(String name)
```

**Parameters**

`name` The region name to set (e.g., "MRZ", "PortraitZone", "SignatureArea").

### setLocation

Sets the location of this auxiliary region.

```java
void setLocation(Quadrilateral location) throws CoreException
```

**Parameters**

`location` A `Quadrilateral` object defining the region boundaries.

**Exception**

Throws a `CoreException` if the operation fails.

**See Also**

[Quadrilateral]({{ site.dcvb_java_api }}core/basic-classes/quadrilateral.html)

### setConfidence

Sets the confidence level of this auxiliary region detection.

```java
void setConfidence(int confidence)
```

**Parameters**

`confidence` The confidence value to set, typically in the range [0, 100].
