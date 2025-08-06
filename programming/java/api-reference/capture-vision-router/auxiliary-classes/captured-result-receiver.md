---
layout: default-layout
title: CapturedResultReceiver Class - Dynamsoft Capture Vision Module Java Edition API Reference
description: Definition of CapturedResultReceiver class in Dynamsoft Capture Vision Module Java Edition.
keywords: captured result receiver, java
---

# CapturedResultReceiver

The `CapturedResultReceiver` class is responsible for receiving captured results. It contains several callback functions for different types of results, including original image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.

## Definition

*Namespace:* com.dynamsoft.cvr

```java
class CapturedResultReceiver
```

## Methods

| Method                                                            | Description                                          |
| ----------------------------------------------------------------- | ---------------------------------------------------- |
| [`onCapturedResultReceived`](#oncapturedresultreceived) | Callback function triggered after processing each image and returns all captured results. |
| [`onOriginalImageResultReceived`](#onoriginalimageresultreceived) | Callback function triggered when start processing each image and returns the original image result. |
| [`onDecodedBarcodesReceived`](#ondecodedbarcodesreceived) | Callback function triggered after processing each image and returns all decoded barcodes results. |
| [`onRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | Callback function triggered after processing each image and returns all recognized text lines results. |
| [`onProcessedDocumentResultReceived`](#onprocesseddocumentresultreceived) | Callback function triggered after processing each image and returns all processed document results.        |
| [`onParsedResultsReceived`](#onparsedresultsreceived) | Callback function triggered after processing each image and returns all parsed results.                |
| [`getName`](#getname)       | Gets the name of the captured result receiver.                                             |
| [`setName`](#setname)       | Sets the name of the captured result receiver.                                             |
| [`getObservedResultItemTypes`](#getobservedresultitemtypes) | Gets the types of result items being observed.                   |

### onCapturedResultReceived

Callback function triggered after processing each image and returns all captured results.

```java
public void onCapturedResultReceived(CapturedResult result)
```

**Parameters**

`result` The captured result.

**See Also**

[CapturedResult]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/captured-result.html)

### onOriginalImageResultReceived

Callback function triggered when start processing each image and returns the original image result. For the callback to be triggered, it is essential that the parameter `OutputOriginalImage` is set to value `1`.

```java
public void onOriginalImageResultReceived(OriginalImageResultItem result)
```

**Parameters**

`result` The original image result.

**See Also**

[OriginalImageResultItem]({{ site.dcvb_java_api }}core/basic-classes/original-image-result-item.html)

### onDecodedBarcodesReceived

Callback function triggered after processing each image and returns all decoded barcodes. For the callback to be triggered, it is essential that the `BarcodeReaderTask` is properly configured.

```java
public void onDecodedBarcodesReceived(DecodedBarcodesResult result)
```

**Parameters**

`result` The decoded barcodes result.

**See Also**

[DecodedBarcodesResult]({{ site.dbr_java_api }}decoded-barcodes-result.html)

### onRecognizedTextLinesReceived

Callback function triggered after processing each image and returns all recognized text lines. For the callback to be triggered, it is essential that the `LabelRecognizerTask` is properly configured.

```java
public void onRecognizedTextLinesReceived(RecognizedTextLinesResult result)
```

**Parameters**

`result` The recognized text lines result.

**See Also**

[RecognizedTextLinesResult]({{ site.dlr_java_api }}recognized-text-lines-result.html)

### onProcessedDocumentResultReceived

Callback function triggered after processing each image and returns all processed document results. For the callback to be triggered, it is essential that the `DocumentNormalizerTask` is properly configured.

```java
public void onProcessedDocumentResultReceived(ProcessedDocumentResult result)
```

**Parameters**

`result` The processed document results.

**See Also**

[ProcessedDocumentResult]({{ site.ddn_java_api }}processed-document-result.html)

### onParsedResultsReceived

Callback function triggered after processing each image and returns all parsed results. For the callback to be triggered, it is essential that the `CodeParserTask` is properly configured.

```java
public void onParsedResultsReceived(ParsedResult result)
```

**Parameters**

`result` The parsed result.

**See Also**

[ParsedResult]({{ site.dcp_java_api }}parsed-result.html)

### getName

Gets the name of the captured result receiver.  

```java
public String getName()
```

**Return Value**

Returns the name of the captured result receiver.  

### setName

Sets the name of the captured result receiver.  

```java
public void setName(String name)
```

**Parameters**

`name` The name of the captured result receiver.

### getObservedResultItemTypes

Gets the types of result items being observed.

```java
public int getObservedResultItemTypes()
```

**Return Value**

Returns an integer representing the types of result items being observed.
