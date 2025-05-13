---
layout: default-layout
title: CapturedResult Class - Dynamsoft Capture Vision Module .NET Edition API Reference
description: Definition of CapturedResult class in Dynamsoft Capture Vision Module .NET Edition.
keywords: captured result, .NET
needAutoGenerateSidebar: true
---

# CapturedResult

The `CapturedResult` class represents the result of a capture operation on an image. Internally, `CaptureResult` stores an array that contains multiple items, each of which may be a barcode, text line, detected quad, normalized image, raw image, parsed item, etc.

## Definition

*Namespace:* Dynamsoft.CVR


```csharp
public abstract class CapturedResult 
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetOriginalImageHashId`](#getoriginalimagehashid) | Gets the hash ID of the original image.|
| [`GetOriginalImageTag`](#getoriginalimagetag) | Gets the tag of the original image.|
| [`GetItems`](#getitems) | Gets all items in the captured result.|
| [`GetRotationTransformMatrix`](#getrotationtransformmatrix) | Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.|
| [`GetErrorCode`](#geterrorcode) | Gets the error code of the capture operation.|
| [`GetErrorString`](#geterrorstring) | Gets the error message of the capture operation.|
| [`GetDecodedBarcodesResult`](#getdecodedbarcodesresult) | Gets the decoded barcode items from the `CapturedResult`.|
| [`GetRecognizedTextLinesResult`](#getrecognizedtextlinesresult) | Gets the recognized text line items from the `CapturedResult`.|
| [`GetDetectedQuadsResult`](#getdetectedquadsresult) | Gets the detected quads items from the `CapturedResult`.|
| [`GetNormalizedImagesResult`](#getnormalizedimagesresult) | Gets the normalized images items from the `CapturedResult`.|
| [`GetParsedResult`](#getparsedresult) | Gets the parsed result items from the `CapturedResult`.|

### GetOriginalImageHashId

Gets the hash ID of the original image.

```csharp
abstract string GetOriginalImageHashId()
```

**Return Value**

Returns the hash ID of the original image as a string.

### GetOriginalImageTag

Gets the tag of the original image.

```csharp
abstract ImageTag GetOriginalImageTag()
```

**Return Value**

Returns an `ImageTag` object containing the tag of the original image.

**See Also**

[ImageTag]({{ site.dcvb_dotnet_api }}core/basic-classes/image-tag.html)

### GetItems

Gets all items in the captured result.

```csharp
abstract CapturedResultItem[] GetItems()
```

**Return Value**

Returns a `CapturedResultItem` array with all items in the captured result.

**See Also**

[CapturedResultItem]({{ site.dcvb_dotnet_api }}core/basic-classes/captured-result-item.html)

### GetRotationTransformMatrix

Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.

```csharp
abstract double[] GetRotationTransformMatrix()
```

**Return Value**

Returns a double array of length 9 which represents a 3x3 rotation matrix.

### GetErrorCode

Gets the error code of the capture operation.

```csharp
abstract int GetErrorCode()
```

**Return Value**

Returns the error code of the capture operation.

**See Also**

[EnumErrorCode]({{ site.dcvb_dotnet_api }}core/enum-error-code.html)

### GetErrorString

Gets the error message of the capture operation.

```csharp
abstract string GetErrorString()
```

**Return Value**

Returns the error message of the capture operation as a string.

### GetDecodedBarcodesResult

Gets the decoded barcode items from the `CapturedResult`.

```csharp
abstract DecodedBarcodesResult GetDecodedBarcodesResult()
```

**Return Value**

Returns a `DecodedBarcodesResult` object containing the decoded barcode items. 

**See Also**

[DecodedBarcodesResult]({{ site.dbr_dotnet_api }}decoded-barcodes-result.html)

### GetRecognizedTextLinesResult

Gets the recognized text line items from the `CapturedResult`.

```csharp
abstract RecognizedTextLinesResult GetRecognizedTextLinesResult()
```

**Return Value**

Returns a `RecognizedTextLinesResult` object containing the recognized text line items.

**See Also**

[RecognizedTextLinesResult]({{ site.dlr_dotnet_api }}recognized-text-lines-result.html)

### GetDetectedQuadsResult

Gets the detected quads items from the `CapturedResult`.

```csharp
abstract DetectedQuadsResult GetDetectedQuadsResult()
```

**Return Value**

Returns a `DetectedQuadsResult` object containing the detected quads items.

**See Also**

[DetectedQuadsResult]({{ site.ddn_dotnet_api }}detected-quads-result.html)

### GetNormalizedImagesResult

Gets the normalized images items from the `CapturedResult`.

```csharp
abstract NormalizedImagesResult GetNormalizedImagesResult()
```

**Return Value**

Returns a `NormalizedImagesResult` object containing the normalized images items.

**See Also**

[NormalizedImagesResult]({{ site.ddn_dotnet_api }}normalized-images-result.html)

### GetParsedResult

Gets the parsed result items from the `CapturedResult`.

```csharp
abstract ParsedResult GetParsedResult()
```

**Return Value**

Returns a `ParsedResult` object containing the parsed result items.

**See Also**

[ParsedResult]({{ site.dcp_dotnet_api }}parsed-result.html)
