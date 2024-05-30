---
layout: default-layout
title: CapturedResultFilter Class - Dynamsoft Capture Vision Module .NET Edition API Reference
description: Definition of CapturedResultFilter class in Dynamsoft Capture Vision Module .NET Edition.
keywords: captured result receiver, .NET
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# CapturedResultFilter

The `CapturedResultFilter` class is responsible for filtering captured results. It contains several callback functions for different types of results, including original image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.

>Note: Currently, user defined `CapturedResultFilter` is not supported.

## Definition

*Namespace:* Dynamsoft.CVR

*Assembly:* Dynamsoft.CaptureVisionRouter.dll

```csharp
public class CapturedResultFilter 
```

## Methods

| Method                                                            | Description                                          |
| ----------------------------------------------------------------- | ---------------------------------------------------- |
| [`OnOriginalImageResultReceived`](#onoriginalimageresultreceived) | Callback function for original image results.        |
| [`OnDecodedBarcodesReceived`](#ondecodedbarcodesreceived)         | Callback function for decoded barcodes results.      |
| [`OnRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | Callback function for recognized text lines results. |
| [`OnDetectedQuadsReceived`](#ondetectedquadsreceived)             | Callback function for detected quads results.        |
| [`OnNormalizedImagesReceived`](#onnormalizedimagesreceived)       | Callback function for normalized images results.     |
| [`OnParsedResultsReceived`](#onparsedresultsreceived)             | Callback function for parsed results.                |
| [`GetName`](#getname)       | Gets the name of the captured result filter.                                             |
| [`SetName`](#setname)       | Sets the name of the captured result filter.                                             |


### OnOriginalImageResultReceived

Callback function for original image results. It will be called once for each original image result.

```csharp
virtual void OnOriginalImageResultReceived(OriginalImageResultItem pResult)
```

**Parameters**

`[in] pResult` The original image result.

**See Also**

[OriginalImageResultItem]({{ site.dcv_dotnet_api }}core/basic-classes/original-image-result-item.html)

### OnDecodedBarcodesReceived

Callback function for decoded barcodes results. It will be called once for each decoded barcodes result.

```csharp
virtual void OnDecodedBarcodesReceived(DecodedBarcodesResult pResult)
```

**Parameters**

`[in] pResult` The decoded barcodes result.

**See Also**

[DecodedBarcodesResult]({{ site.dbr_dotnet_api }}decoded-barcodes-result.html)

### OnRecognizedTextLinesReceived

Callback function for recognized text lines results. It will be called once for each recognized text lines result.

```csharp
virtual void OnRecognizedTextLinesReceived(RecognizedTextLinesResult pResult)
```

**Parameters**

`[in] pResult` The recognized text lines result.

**See Also**

[RecognizedTextLinesResult]({{ site.dlr_dotnet_api }}recognized-text-lines-result.html)

### OnDetectedQuadsReceived

Callback function for detected quads results. It will be called once for each detected quads result.

```csharp
virtual void OnDetectedQuadsReceived(DetectedQuadsResult pResult)
```

**Parameters**

`[in] pResult` The detected quads result.

**See Also**

[DetectedQuadsResult]({{ site.ddn_dotnet_api }}detected-quads-result.html)

### OnNormalizedImagesReceived

Callback function for normalized images results. It will be called once for each normalized images result.

```csharp
virtual void OnNormalizedImagesReceived(NormalizedImagesResult pResult)
```

**Parameters**

`[in] pResult` The normalized images result.

**See Also**

[NormalizedImagesResult]({{ site.ddn_dotnet_api }}normalized-images-result.html)

### OnParsedResultsReceived

Callback function for parsed results. It will be called once for each parsed result.

```csharp
virtual void OnParsedResultsReceived(ParsedResult pResult)
```

**Parameters**

`[in] pResult` The parsed result.

**See Also**

[ParsedResult]({{ site.dcp_dotnet_api }}parsed-result.html)

### GetName

Gets the name of the captured result filter.  

```csharp
string GetName()
```

**Return Value**

Returns the name of the captured result filter.  

### SetName

Sets the name of the captured result filter.  

```csharp
void SetName(string name)
```

**Parameters**

`[in] name` The name of the captured result filter.
