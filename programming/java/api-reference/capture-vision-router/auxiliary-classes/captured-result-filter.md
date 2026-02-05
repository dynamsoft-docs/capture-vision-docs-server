---
layout: default-layout
title: CapturedResultFilter Class - Dynamsoft Capture Vision Module Java Edition API Reference
description: Definition of CapturedResultFilter class in Dynamsoft Capture Vision Module Java Edition.
keywords: captured result filter, java
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# CapturedResultFilter

The `CapturedResultFilter` class is responsible for filtering captured results. It contains several callback functions for different types of results, including original image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.

## Definition

*Package:* com.dynamsoft.cvr

```java
class CapturedResultFilter
```

## Methods

| Method                                                            | Description                                          |
| ----------------------------------------------------------------- | ---------------------------------------------------- |
| [`getName`](#getname)       | Gets the name of the captured result filter.                                             |
| [`setName`](#setname)       | Sets the name of the captured result filter.                                             |
| [`getFilteredResultItemTypes`](#getfilteredresultitemtypes) | Gets the types of result items being filtered.                   |
| [`onOriginalImageResultReceived`](#onoriginalimageresultreceived) | Callback for filtering original image results. |
| [`onDecodedBarcodesReceived`](#ondecodedbarcodesreceived) | Callback for filtering decoded barcode results. |
| [`onRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | Callback for filtering recognized text line results. |

### getName

Gets the name of the captured result filter.  

```java
public String getName()
```

**Return Value**

Returns the name of the captured result filter.  

### setName

Sets the name of the captured result filter.  

```java
public void setName(String name)
```

**Parameters**

`name` The name of the captured result filter.

### getFilteredResultItemTypes

Gets the types of result items being filtered.

```java
public int getFilteredResultItemTypes()
```

**Return Value**

Returns an integer representing the types of result items being filtered.

### onOriginalImageResultReceived

Callback function for filtering original image results.

```java
public void onOriginalImageResultReceived(OriginalImageResultItem result)
```

**Parameters**

`result` The original image result to be filtered.

**See Also**

[OriginalImageResultItem]({{ site.dcvb_java_api }}core/basic-classes/original-image-result-item.html)

### onDecodedBarcodesReceived

Callback function for filtering decoded barcode results.

```java
public void onDecodedBarcodesReceived(DecodedBarcodesResult result)
```

**Parameters**

`result` The decoded barcodes result to be filtered.

**See Also**

[DecodedBarcodesResult]({{ site.dbr_java_api }}decoded-barcodes-result.html)

### onRecognizedTextLinesReceived

Callback function for filtering recognized text line results.

```java
public void onRecognizedTextLinesReceived(RecognizedTextLinesResult result)
```

**Parameters**

`result` The recognized text lines result to be filtered.

**See Also**

[RecognizedTextLinesResult]({{ site.dlr_java_api }}recognized-text-lines-result.html)
