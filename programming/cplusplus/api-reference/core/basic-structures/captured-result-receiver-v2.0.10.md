---
layout: default-layout
title: class CCapturedResultReceiver - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the C++ edition of the class CCapturedResultReceiver in Core Module.
keywords: captured result receiver, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: C++ CCapturedResultReceiver Class
permalink: /programming/cplusplus/api-reference/core/basic-structures/captured-result-receiver.html
---

# CCapturedResultReceiver

The `CCapturedResultReceiver` class is responsible for receiving captured results. It contains several callback functions for different types of results, including original image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore

```cpp
class CCapturedResultReceiver 
```

## Methods Summary

| Method                                                            | Description                                          |
| ----------------------------------------------------------------- | ---------------------------------------------------- |
| [`CCapturedResultReceiver`](#ccapturedresultreceiver-constructor)               | Constructor                                          |
| [`~CCapturedResultReceiver`](#ccapturedresultreceiver-destructor)              | Destructor                                           |
| [`GetObservedResultItemTypes`](#getobservedresultitemtypes)       | Gets the types of observed result items.             |
| [`OnCapturedResultReceived`](#oncapturedresultreceived)           | Callback function for all captured results.          |
| [`OnOriginalImageResultReceived`](#onoriginalimageresultreceived)           | Callback function for original image results.             |
| [`OnDecodedBarcodesReceived`](#ondecodedbarcodesreceived)         | Callback function for decoded barcodes results.      |
| [`OnRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | Callback function for recognized text lines results. |
| [`OnDetectedQuadsReceived`](#ondetectedquadsreceived)             | Callback function for detected quads results.        |
| [`OnNormalizedImagesReceived`](#onnormalizedimagesreceived)       | Callback function for normalized images results.     |
| [`OnParsedResultsReceived`](#onparsedresultsreceived)             | Callback function for parsed results.                |
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

Callback function for all captured results. It will be called once for each captured result.

```cpp
virtual void OnCapturedResultReceived(const CCapturedResult* pResult)
```

**Parameters**

`[in] pResult` The captured result.

### OnOriginalImageResultReceived

Callback function for original image results. It will be called once for each original image result.

```cpp
virtual void OnOriginalImageResultReceived(const COriginalImageResultItem* pResult)
```

**Parameters**

`[in] pResult` The original image result.

### OnDecodedBarcodesReceived

Callback function for decoded barcodes results. It will be called once for each decoded barcodes result.

```cpp
virtual void OnDecodedBarcodesReceived(const dbr::CDecodedBarcodesResult* pResult)
```

**Parameters**

`[in] pResult` The decoded barcodes result.

### OnRecognizedTextLinesReceived

Callback function for recognized text lines results. It will be called once for each recognized text lines result.

```cpp
virtual void OnRecognizedTextLinesReceived(const dlr::CRecognizedTextLinesResult* pResult)
```

**Parameters**

`[in] pResult` The recognized text lines result.

### OnDetectedQuadsReceived

Callback function for detected quads results. It will be called once for each detected quads result.

```cpp
virtual void OnDetectedQuadsReceived(const ddn::CDetectedQuadsResult* pResult)
```

**Parameters**

`[in] pResult` The detected quads result.

### OnNormalizedImagesReceived

Callback function for normalized images results. It will be called once for each normalized images result.

```cpp
virtual void OnNormalizedImagesReceived(const ddn::CNormalizedImagesResult* pResult)
```

**Parameters**

`[in] pResult` The normalized images result.

### OnParsedResultsReceived

Callback function for parsed results. It will be called once for each parsed result.

```cpp
virtual void OnParsedResultsReceived(const dcp::CParsedResult* pResult)
```

**Parameters**

`[in] pResult` The parsed result.

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
