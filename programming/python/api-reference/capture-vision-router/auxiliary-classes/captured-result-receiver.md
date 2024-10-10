---
layout: default-layout
title: CapturedResultReceiver Class - Dynamsoft Capture Vision Module Python Edition API Reference
description: Definition of CapturedResultReceiver class in Dynamsoft Capture Vision Module Python Edition.
keywords: captured result receiver, python
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# CapturedResultReceiver

The `CapturedResultReceiver` class is responsible for receiving captured results. It contains several callback functions for different types of results, including original image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.

## Definition

*Module:* dynamsoft_capture_vision_router

```python
class CapturedResultReceiver(ABC)
```

## Methods

| Method                                                            | Description                                          |
| ----------------------------------------------------------------- | ---------------------------------------------------- |
| [`on_captured_result_received`](#on_captured_result_received)           | Callback function triggered after processing each image and returns all captured results.          |
| [`on_original_image_result_received`](#on_original_image_result_received) | Callback function triggered when start processing each image and returns the original image result.        |
| [`on_decoded_barcodes_received`](#on_decoded_barcodes_received)         | Callback function triggered after processing each image and returns all decoded barcodes results.      |
| [`on_recognized_text_lines_received`](#on_recognized_text_lines_received) | Callback function triggered after processing each image and returns all recognized text lines results. |
| [`on_detected_quads_received`](#on_detected_quads_received)             | Callback function triggered after processing each image and returns all detected quads results.        |
| [`on_normalized_images_received`](#on_normalized_images_received)       | Callback function triggered after processing each image and returns all normalized images results.     |
| [`on_parsed_results_received`](#on_parsed_results_received)             | Callback function triggered after processing each image and returns all parsed results.                |
| [`get_name`](#get_name)       | Gets the name of the captured result receiver.                                             |
| [`set_name`](#set_name)       | Sets the name of the captured result receiver.                                             |

### on_captured_result_received

Callback function triggered after processing each image and returns all captured results.

```python
def on_captured_result_received(self, result: CapturedResult) -> None:
```

**Parameters**

`result` The captured result.

**See Also**

[CapturedResult]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/captured-result.html)

### on_original_image_result_received

Callback function triggered when start processing each image and returns the original image result. For the callback to be triggered, it is essential that the parameter `OutputOriginalImage` is set to value `1`.

```python
def on_original_image_result_received(self, result: OriginalImageResultItem) -> None:
```

**Parameters**

`result` The original image result.

**See Also**

[OriginalImageResultItem]({{ site.dcvb_python_api }}core/basic-classes/original-image-result-item.html)

### on_decoded_barcodes_received

Callback function triggered after processing each image and returns all decoded barcodes. For the callback to be triggered, it is essential that the `BarcodeReaderTask` is properly configured.

```python
def on_decoded_barcodes_received(self, result: "DecodedBarcodesResult") -> None:
```

**Parameters**

`result` The decoded barcodes result.

**See Also**

[DecodedBarcodesResult]({{ site.dbr_python_api }}decoded-barcodes-result.html)

### on_recognized_text_lines_received

Callback function triggered after processing each image and returns all recognized text lines. For the callback to be triggered, it is essential that the `LabelRecognizerTask` is properly configured.

```python
def on_recognized_text_lines_received(self, result: "RecognizedTextLinesResult") -> None:
```

**Parameters**

`result` The recognized text lines result.

**See Also**

[RecognizedTextLinesResult]({{ site.dlr_python_api }}recognized-text-lines-result.html)

### on_detected_quads_received

Callback function triggered after processing each image and returns all detected quads. For the callback to be triggered, it is essential that the `DocumentNormalizerTask` is properly configured.

```python
def on_detected_quads_received(self, result: "DetectedQuadsResult") -> None:
```

**Parameters**

`result` The detected quads result.

**See Also**

[DetectedQuadsResult]({{ site.ddn_python_api }}detected-quads-result.html)

### on_normalized_images_received

Callback function triggered after processing each image and returns all normalized images. For the callback to be triggered, it is essential that the `DocumentNormalizerTask` is properly configured.

```python
def on_normalized_images_received(self, result: "NormalizedImagesResult") -> None:
```

**Parameters**

`result` The normalized images result.

**See Also**

[NormalizedImagesResult]({{ site.ddn_python_api }}normalized-images-result.html)

### on_parsed_results_received

Callback function triggered after processing each image and returns all parsed results. For the callback to be triggered, it is essential that the `CodeParserTask` is properly configured.

```python
def on_parsed_results_received(self, result: "ParsedResult") -> None:
```

**Parameters**

`result` The parsed result.

**See Also**

[ParsedResult]({{ site.dcp_python_api }}parsed-result.html)

### get_name

Gets the name of the captured result receiver.  

```python
def get_name(self) -> str:
```

**Return Value**

Returns the name of the captured result receiver.  

### set_name

Sets the name of the captured result receiver.  

```python
def set_name(self, name: str) -> None:
```

**Parameters**

`name` The name of the captured result receiver.
