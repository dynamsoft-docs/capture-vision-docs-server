---
layout: default-layout
title: CapturedResultReceiver Class - Dynamsoft Capture Vision Module .NET Edition API Reference
description: Definition of CapturedResultReceiver class in Dynamsoft Capture Vision Module .NET Edition.
keywords: captured result receiver, .NET
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# CapturedResultReceiver

The `CapturedResultReceiver` class is responsible for receiving captured results. It contains several callback functions for different types of results, including original image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.

## Definition

*Namespace:* Dynamsoft.CVR


```csharp
public class CapturedResultReceiver 
```

## Methods

| Method                                                            | Description                                          |
| ----------------------------------------------------------------- | ---------------------------------------------------- |
| [`OnCapturedResultReceived`](#oncapturedresultreceived)           | Callback function triggered after processing each image and returns all captured results.          |
| [`OnOriginalImageResultReceived`](#onoriginalimageresultreceived) | Callback function triggered when start processing each image and returns the original image result.        |
| [`OnDecodedBarcodesReceived`](#ondecodedbarcodesreceived)         | Callback function triggered after processing each image and returns all decoded barcodes results.      |
| [`OnRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | Callback function triggered after processing each image and returns all recognized text lines results. |
| [`OnDetectedQuadsReceived`](#ondetectedquadsreceived)             | Callback function triggered after processing each image and returns all detected quads results.        |
| [`OnNormalizedImagesReceived`](#onnormalizedimagesreceived)       | Callback function triggered after processing each image and returns all normalized images results.     |
| [`OnParsedResultsReceived`](#onparsedresultsreceived)             | Callback function triggered after processing each image and returns all parsed results.                |
| [`GetName`](#getname)       | Gets the name of the captured result receiver.                                             |
| [`SetName`](#setname)       | Sets the name of the captured result receiver.                                             |

### OnCapturedResultReceived

Callback function triggered after processing each image and returns all captured results.

```csharp
virtual void OnCapturedResultReceived(CapturedResult result)
```

**Parameters**

`[in] result` The captured result.

**See Also**

[CapturedResult]({{ site.dcvb_dotnet_api }}capture-vision-router/auxiliary-classes/captured-result.html)

### OnOriginalImageResultReceived

Callback function triggered when start processing each image and returns the original image result. For the callback to be triggered, it is essential that the parameter `OutputOriginalImage` is set to value `1`.

```csharp
virtual void OnOriginalImageResultReceived(OriginalImageResultItem result)
```

**Parameters**

`[in] result` The original image result.

**See Also**

[OriginalImageResultItem]({{ site.dcvb_dotnet_api }}core/basic-classes/original-image-result-item.html)

### OnDecodedBarcodesReceived

Callback function triggered after processing each image and returns all decoded barcodes. For the callback to be triggered, it is essential that the `BarcodeReaderTask` is properly configured.

```csharp
virtual void OnDecodedBarcodesReceived(DecodedBarcodesResult result)
```

**Parameters**

`[in] result` The decoded barcodes result.

**See Also**

[DecodedBarcodesResult]({{ site.dbr_dotnet_api }}decoded-barcodes-result.html)

### OnRecognizedTextLinesReceived

Callback function triggered after processing each image and returns all recognized text lines. For the callback to be triggered, it is essential that the `LabelRecognizerTask` is properly configured.

```csharp
virtual void OnRecognizedTextLinesReceived(RecognizedTextLinesResult result)
```

**Parameters**

`[in] result` The recognized text lines result.

**See Also**

[RecognizedTextLinesResult]({{ site.dlr_dotnet_api }}recognized-text-lines-result.html)

### OnDetectedQuadsReceived

Callback function triggered after processing each image and returns all detected quads. For the callback to be triggered, it is essential that the `DocumentNormalizerTask` is properly configured.

```csharp
virtual void OnDetectedQuadsReceived(DetectedQuadsResult result)
```

**Parameters**

`[in] result` The detected quads result.

**See Also**

[DetectedQuadsResult]({{ site.ddn_dotnet_api }}detected-quads-result.html)

### OnNormalizedImagesReceived

Callback function triggered after processing each image and returns all normalized images. For the callback to be triggered, it is essential that the `DocumentNormalizerTask` is properly configured.

```csharp
virtual void OnNormalizedImagesReceived(NormalizedImagesResult result)
```

**Parameters**

`[in] result` The normalized images result.

**See Also**

[NormalizedImagesResult]({{ site.ddn_dotnet_api }}normalized-images-result.html)

### OnParsedResultsReceived

Callback function triggered after processing each image and returns all parsed results. For the callback to be triggered, it is essential that the `CodeParserTask` is properly configured.

```csharp
virtual void OnParsedResultsReceived(ParsedResult result)
```

**Parameters**

`[in] result` The parsed result.

**See Also**

[ParsedResult]({{ site.dcp_dotnet_api }}parsed-result.html)

### GetName

Gets the name of the captured result receiver.  

```csharp
string GetName()
```

**Return Value**

Returns the name of the captured result receiver.  

### SetName

Sets the name of the captured result receiver.  

```csharp
void SetName(string name)
```

**Parameters**

`[in] name` The name of the captured result receiver.
