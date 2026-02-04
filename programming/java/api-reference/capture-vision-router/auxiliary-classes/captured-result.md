---
layout: default-layout
title: CapturedResult Class - Dynamsoft Capture Vision Module Java Edition API Reference
description: Definition of CapturedResult class in Dynamsoft Capture Vision Module Java Edition.
keywords: captured result, java
needAutoGenerateSidebar: true
---

# CapturedResult

The `CapturedResult` class represents the result of a capture operation on an image. Internally, `CapturedResult` stores an array that contains multiple items, each of which may be a barcode, text line, detected quad, normalized image, raw image, parsed item, etc.

## Definition

*Package:* com.dynamsoft.cvr

```java
class CapturedResult extends CapturedResultBase
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`getOriginalImageHashId`](#getoriginalimagehashid) | Gets the hash ID of the original image.|
| [`getOriginalImageTag`](#getoriginalimagetag) | Gets the tag of the original image.|
| [`getItems`](#getitems) | Gets all items in the captured result.|
| [`getItem`](#getitem) | Gets a specific item by index.|
| [`getItemsCount`](#getitemscount) | Gets the count of items in the captured result.|
| [`getRotationTransformMatrix`](#getrotationtransformmatrix) | Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.|
| [`getErrorCode`](#geterrorcode) | Gets the error code of the capture operation.|
| [`getErrorString`](#geterrorstring) | Gets the error message of the capture operation.|
| [`getDecodedBarcodesResult`](#getdecodedbarcodesresult) | Gets the decoded barcode items from the `CapturedResult`.|
| [`getRecognizedTextLinesResult`](#getrecognizedtextlinesresult) | Gets the recognized text line items from the `CapturedResult`.|
| [`getProcessedDocumentResult`](#getprocesseddocumentresult) | Gets the processed document items from the `CapturedResult`.|
| [`getParsedResult`](#getparsedresult) | Gets the parsed result items from the `CapturedResult`.|

### getOriginalImageHashId

Gets the hash ID of the original image.

```java
public String getOriginalImageHashId()
```

**Return Value**

Returns the hash ID of the original image as a string.

### getOriginalImageTag

Gets the tag of the original image.

```java
public ImageTag getOriginalImageTag()
```

**Return Value**

Returns an `ImageTag` object containing the tag of the original image.

**See Also**

[ImageTag]({{ site.dcvb_java_api }}core/basic-classes/image-tag.html)

### getItems

Gets all items in the captured result.

```java
public CapturedResultItem[] getItems()
```

**Return Value**

Returns a `CapturedResultItem` array with all items in the captured result.

**See Also**

[CapturedResultItem]({{ site.dcvb_java_api }}core/basic-classes/captured-result-item.html)

### getItem

Gets a specific item by index.

```java
public CapturedResultItem getItem(int index)
```

**Parameters**

`index` The index of the item to retrieve.

**Return Value**

Returns a `CapturedResultItem` object at the specified index.

**See Also**

[CapturedResultItem]({{ site.dcvb_java_api }}core/basic-classes/captured-result-item.html)

### getItemsCount

Gets the count of items in the captured result.

```java
public int getItemsCount()
```

**Return Value**

Returns the number of items in the captured result.

### getRotationTransformMatrix

Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.

```java
public double[] getRotationTransformMatrix()
```

**Return Value**

Returns a double array of length 9 which represents a 3x3 rotation matrix.

### getErrorCode

Gets the error code of the capture operation.

```java
public int getErrorCode()
```

**Return Value**

Returns the error code of the capture operation.

### getErrorString

Gets the error message of the capture operation.

```java
public String getErrorString()
```

**Return Value**

Returns the error message of the capture operation as a string.

### getDecodedBarcodesResult

Gets the decoded barcode items from the `CapturedResult`.

```java
public DecodedBarcodesResult getDecodedBarcodesResult()
```

**Return Value**

Returns a `DecodedBarcodesResult` object containing the decoded barcode items. 

**See Also**

[DecodedBarcodesResult]({{ site.dbr_java_api }}decoded-barcodes-result.html)

### getRecognizedTextLinesResult

Gets the recognized text line items from the `CapturedResult`.

```java
public RecognizedTextLinesResult getRecognizedTextLinesResult()
```

**Return Value**

Returns a `RecognizedTextLinesResult` object containing the recognized text line items.

**See Also**

[RecognizedTextLinesResult]({{ site.dlr_java_api }}recognized-text-lines-result.html)

### getProcessedDocumentResult

Gets the processed document items from the `CapturedResult`.

```java
public ProcessedDocumentResult getProcessedDocumentResult()
```

**Return Value**

Returns a `ProcessedDocumentResult` object containing the processed document items.

**See Also**

[ProcessedDocumentResult]({{ site.ddn_java_api }}processed-document-result.html)

### getParsedResult

Gets the parsed result items from the `CapturedResult`.

```java
public ParsedResult getParsedResult()
```

**Return Value**

Returns a `ParsedResult` object containing the parsed result items.

**See Also**

[ParsedResult]({{ site.dcp_java_api }}parsed-result.html)
