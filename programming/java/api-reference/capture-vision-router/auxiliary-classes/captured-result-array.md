---
layout: default-layout
title: CapturedResult Array - Dynamsoft Capture Vision Module Java Edition API Reference
description: Definition of CapturedResult array in Dynamsoft Capture Vision Module Java Edition.
keywords: captured result, java
needAutoGenerateSidebar: true
---

# CapturedResult Array

In the Java Edition, multiple `CapturedResult` objects are returned as a simple Java array `CapturedResult[]`, rather than a specialized collection class. This array represents a collection of `CapturedResult` objects, each derived from a capture operation on an image. Each `CapturedResult` contains items which may include barcodes, text lines, detected quads, normalized images, raw images, parsed items, and more.

## Definition

*Namespace:* com.dynamsoft.cvr

```java
CapturedResult[]
```

## Usage

The `CapturedResult[]` array is returned by methods such as `captureMultiPages()` and can be used with standard Java array operations:

```java
// Get results from multi-page capture
CapturedResult[] results = cvr.captureMultiPages(filePath);

// Iterate through results
for (CapturedResult result : results) {
    // Process each result
}

// Access by index
CapturedResult firstResult = results[0];

// Get array length
int count = results.length;
```

**See Also**

[CapturedResult]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/captured-result.html)

