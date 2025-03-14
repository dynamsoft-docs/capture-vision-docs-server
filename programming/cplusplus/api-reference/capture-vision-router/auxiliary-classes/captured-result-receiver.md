---
layout: default-layout
title: class CCapturedResultReceiver - Dynamsoft Capture Vision C++ Edition API Reference
description: The class CCapturedResultReceiver of CaptureVisionRouter module C++ edition is responsible for receiving captured results.
keywords: captured result receiver, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: C++ CCapturedResultReceiver Class
---

# CCapturedResultReceiver

The `CCapturedResultReceiver` class is responsible for receiving captured results. It contains several callback functions for different types of results, including original image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.

## Definition

*Namespace:* dynamsoft::cvr

*Assembly:* DynamsoftCaptureVisionRouter

```cpp
class CCapturedResultReceiver 
```

## Methods Summary

| Method                                                            | Description                                          |
| ----------------------------------------------------------------- | ---------------------------------------------------- |
| [`CCapturedResultReceiver`](#ccapturedresultreceiver-constructor) | Constructor                                          |
| [`~CCapturedResultReceiver`](#ccapturedresultreceiver-destructor) | Destructor                                           |
| [`GetObservedResultItemTypes`](#getobservedresultitemtypes)       | Gets the types of observed result items.             |
| [`OnCapturedResultReceived`](#oncapturedresultreceived)           | Callback function triggered after processing each image and returns all captured results.          |
| [`OnOriginalImageResultReceived`](#onoriginalimageresultreceived) | Callback function triggered when start processing each image and returns the original image result.        |
| [`OnDecodedBarcodesReceived`](#ondecodedbarcodesreceived)         | Callback function triggered after processing each image and returns all decoded barcodes results.      |
| [`OnRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | Callback function triggered after processing each image and returns all recognized text lines results. |
| [`OnProcessedDocumentResultReceived`](#onprocesseddocumentresultreceived)       | Callback function triggered after processing each image and returns all  processed document results.  |
| [`OnParsedResultsReceived`](#onparsedresultsreceived)             | Callback function triggered after processing each image and returns all parsed results.                |
| [`GetName`](#getname)       | Gets the name of the captured result receiver.                                             |
| [`SetName`](#setname)       | Sets the name of the captured result receiver.                                             |

### CCapturedResultReceiver Constructor

Constructor.

```cpp
CCapturedResultReceiver()
```

### CCapturedResultReceiver Destructor

Destructor.

```cpp
virtual ~CCapturedResultReceiver()
```

### GetObservedResultItemTypes

Gets the types of observed result items.

```cpp
unsigned int GetObservedResultItemTypes()
```

**Return value**

Returns the types of observed result items.

### OnCapturedResultReceived

Callback function triggered after processing each image and returns all captured results.

```cpp
virtual void OnCapturedResultReceived(CCapturedResult* pResult)
```

**Parameters**

`[in] pResult` The captured result.

**See Also**

[CCapturedResult]({{ site.dcvb_cpp_api }}capture-vision-router/auxiliary-classes/captured-result.html)

### OnOriginalImageResultReceived

Callback function triggered when start processing each image and returns the original image result. For the callback to be triggered, it is essential that the parameter `OutputOriginalImage` is set to value `1`.

```cpp
virtual void OnOriginalImageResultReceived(COriginalImageResultItem* pResult)
```

**Parameters**

`[in] pResult` The original image result.

**See Also**

[COriginalImageResultItem]({{ site.dcvb_cpp_api }}core/basic-structures/original-image-result-item.html)

### OnDecodedBarcodesReceived

Callback function triggered after processing each image and returns all decoded barcodes. For the callback to be triggered, it is essential that the `BarcodeReaderTask` is properly configured.

```cpp
virtual void OnDecodedBarcodesReceived(dbr::CDecodedBarcodesResult* pResult)
```

**Parameters**

`[in] pResult` The decoded barcodes result.

**See Also**

[CDecodedBarcodesResult]({{ site.dbr_cpp_api }}decoded-barcodes-result.html)

### OnRecognizedTextLinesReceived

Callback function triggered after processing each image and returns all recognized text lines. For the callback to be triggered, it is essential that the `LabelRecognizerTask` is properly configured.

```cpp
virtual void OnRecognizedTextLinesReceived(dlr::CRecognizedTextLinesResult* pResult)
```

**Parameters**

`[in] pResult` The recognized text lines result.

**See Also**

[CRecognizedTextLinesResult]({{ site.dlr_cpp_api }}recognized-text-lines-result.html)

### OnProcessedDocumentResultReceived

Callback function triggered after processing each image and returns all processed document results. For the callback to be triggered, it is essential that the `DocumentNormalizerTask` is properly configured.

```cpp
virtual void OnProcessedDocumentResultReceived(ddn::CProcessedDocumentResult* pResult)
```

**Parameters**

`[in] pResult` The processed document results.

**See Also**

[CProcessedDocumentResult]({{ site.ddn_cpp_api }}processed-document-result.html)

### OnParsedResultsReceived

Callback function triggered after processing each image and returns all parsed results. For the callback to be triggered, it is essential that the `CodeParserTask` is properly configured.

```cpp
virtual void OnParsedResultsReceived(dcp::CParsedResult* pResult)
```

**Parameters**

`[in] pResult` The parsed result.

**See Also**

[CParsedResult]({{ site.dcp_cpp_api }}parsed-result.html)

### GetName

Gets the name of the captured result receiver.  

```cpp
const char* GetName() const
```

**Return value**

Returns the name of the captured result receiver.  

### SetName

Sets the name of the captured result receiver.  

```cpp
void SetName(const char* name)
```

**Parameters**

`[in] name` The name of the captured result receiver.
