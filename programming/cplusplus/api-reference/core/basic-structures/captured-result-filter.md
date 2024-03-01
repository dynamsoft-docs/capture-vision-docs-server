---
layout: default-layout
title: class CCapturedResultFilter - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the C++ edition of the class CCapturedResultFilter in Core Module.
keywords: captured result receiver, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: C++ CCapturedResultFilter Class
permalink: /programming/cplusplus/api-reference/core/basic-structures/captured-result-filter.html
ignore: true
---

# CCapturedResultFilter

The `CCapturedResultFilter` class is responsible for filtering captured results. It contains several callback functions for different types of results, including original image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.

>Note: Currently, user defined CCapturedResultFilter is not supported.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore

```cpp
class CCapturedResultFilter 
```

## Methods Summary

| Method                                                            | Description                                          |
| ----------------------------------------------------------------- | ---------------------------------------------------- |
| [`CCapturedResultFilter`](#ccapturedresultfilter-constructor)               | Constructor                                          |
| [`~CCapturedResultFilter`](#ccapturedresultfilter-destructor)              | Destructor                                           |
| [`GetFilteredResultItemTypes`](#getfilteredresultitemtypes)       | Gets the types of observed result items.             |
| [`OnOriginalImageResultReceived`](#onoriginalimageresultreceived)           | Callback function for original image results.             |
| [`OnDecodedBarcodesReceived`](#ondecodedbarcodesreceived)         | Callback function for decoded barcodes results.      |
| [`OnRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | Callback function for recognized text lines results. |
| [`OnDetectedQuadsReceived`](#ondetectedquadsreceived)             | Callback function for detected quads results.        |
| [`OnNormalizedImagesReceived`](#onnormalizedimagesreceived)       | Callback function for normalized images results.     |
| [`OnParsedResultsReceived`](#onparsedresultsreceived)             | Callback function for parsed results.                |
| [`GetName`](#getname)       | Gets the name of the captured result filter.                                             |
| [`SetName`](#setname)       | Sets the name of the captured result filter.                                             |

### CCapturedResultFilter Constructor

Constructor.

```cpp
CCapturedResultFilter()
```

### CCapturedResultFilter Destructor

Destructor.

```cpp
virtual ~CCapturedResultFilter()
```

### GetFilteredResultItemTypes

Gets the types of filtered result items.

```cpp
unsigned int GetFilteredResultItemTypes()
```

**Return value**

Returns the type [`CapturedResultItemType`]({{site.dcv_enumerations}}core/captured-result-item-type.html?src=cpp&&lang=cpp) of filtered result items.

### OnOriginalImageResultReceived

Callback function for original image results. It will be called once for each original image result.

```cpp
virtual void OnOriginalImageResultReceived(COriginalImageResultItem* pResult)
```

**Parameters**

`[in] pResult` The original image result.

### OnDecodedBarcodesReceived

Callback function for decoded barcodes results. It will be called once for each decoded barcodes result.

```cpp
virtual void OnDecodedBarcodesReceived(dbr::CDecodedBarcodesResult* pResult)
```

**Parameters**

`[in] pResult` The decoded barcodes result.

### OnRecognizedTextLinesReceived

Callback function for recognized text lines results. It will be called once for each recognized text lines result.

```cpp
virtual void OnRecognizedTextLinesReceived(dlr::CRecognizedTextLinesResult* pResult)
```

**Parameters**

`[in] pResult` The recognized text lines result.

### OnDetectedQuadsReceived

Callback function for detected quads results. It will be called once for each detected quads result.

```cpp
virtual void OnDetectedQuadsReceived(ddn::CDetectedQuadsResult* pResult)
```

**Parameters**

`[in] pResult` The detected quads result.

### OnNormalizedImagesReceived

Callback function for normalized images results. It will be called once for each normalized images result.

```cpp
virtual void OnNormalizedImagesReceived(ddn::CNormalizedImagesResult* pResult)
```

**Parameters**

`[in] pResult` The normalized images result.

### OnParsedResultsReceived

Callback function for parsed results. It will be called once for each parsed result.

```cpp
virtual void OnParsedResultsReceived(dcp::CParsedResult* pResult)
```

**Parameters**

`[in] pResult` The parsed result.

### GetName

Gets the name of the captured result filter.  

```cpp
const char* GetName() const
```

**Return value**

Returns the name of the captured result filter.  

### SetName

Sets the name of the captured result filter.  

```cpp
void SetName(const char* name)
```

**Parameters**

`[in] name` The name of the captured result filter.
