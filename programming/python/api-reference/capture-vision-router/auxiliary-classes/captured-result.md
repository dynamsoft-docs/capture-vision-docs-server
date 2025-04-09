---
layout: default-layout
title: CapturedResult Class - Dynamsoft Capture Vision Module Python Edition API Reference
description: Definition of CapturedResult class in Dynamsoft Capture Vision Module Python Edition.
keywords: captured result, python
needAutoGenerateSidebar: true
---

# CapturedResult

The `CapturedResult` class represents the result of a capture operation on an image. Internally, `CaptureResult` stores an array that contains multiple items, each of which may be a barcode, text line, detected quad, normalized image, raw image, parsed item, etc.

## Definition

*Module:* dynamsoft_capture_vision_router

```python
class CapturedResult 
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`get_original_image_hash_id`](#get_original_image_hash_id) | Gets the hash ID of the original image.|
| [`get_original_image_tag`](#get_original_image_tag) | Gets the tag of the original image.|
| [`get_items`](#get_items) | Gets all items in the captured result.|
| [`get_rotation_transform_matrix`](#get_rotation_transform_matrix) | Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.|
| [`get_error_code`](#get_error_code) | Gets the error code of the capture operation.|
| [`get_error_string`](#get_error_string) | Gets the error message of the capture operation.|
| [`get_decoded_barcodes_result`](#get_decoded_barcodes_result) | Gets the decoded barcode items from the `CapturedResult`.|
| [`get_recognized_text_lines_result`](#get_recognized_text_lines_result) | Gets the recognized text line items from the `CapturedResult`.|
| [`get_detected_quads_result`](#get_detected_quads_result) | Gets the detected quads items from the `CapturedResult`.|
| [`get_normalized_images_result`](#get_normalized_images_result) | Gets the normalized images items from the `CapturedResult`.|
| [`get_parsed_result`](#get_parsed_result) | Gets the parsed result items from the `CapturedResult`.|

### get_original_image_hash_id

Gets the hash ID of the original image.

```python
def get_original_image_hash_id(self) -> str:
```

**Return Value**

Returns the hash ID of the original image as a string.

### get_original_image_tag

Gets the tag of the original image.

```python
def get_original_image_tag(self) -> ImageTag:
```

**Return Value**

Returns an `ImageTag` object containing the tag of the original image.

**See Also**

[ImageTag]({{ site.dcvb_python_api }}core/basic-classes/image-tag.html)

### get_items

Gets all items in the captured result.

```python
def get_items(self) -> List[CapturedResultItem]:
```

**Return Value**

Returns a `CapturedResultItem` list with all items in the captured result.

**See Also**

[CapturedResultItem]({{ site.dcvb_python_api }}core/basic-classes/captured-result-item.html)

### get_rotation_transform_matrix

Gets the 3x3 rotation transformation matrix of the original image relative to the rotated image.

```python
def get_rotation_transform_matrix(self) -> List[float]:
```

**Return Value**

Returns a float list of length 9 which represents a 3x3 rotation matrix.

### get_error_code

Gets the error code of the capture operation.

```python
def get_error_code(self) -> int:
```

**Return Value**

Returns the error code of the capture operation.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html)

### get_error_string

Gets the error message of the capture operation.

```python
def get_error_string(self) -> str:
```

**Return Value**

Returns the error message of the capture operation as a string.

### get_decoded_barcodes_result

Gets the decoded barcode items from the `CapturedResult`.

```python
def get_decoded_barcodes_result(self) -> "DecodedBarcodesResult":
```

**Return Value**

Returns a `DecodedBarcodesResult` object containing the decoded barcode items. 

**See Also**

[DecodedBarcodesResult]({{ site.dbr_python_api }}decoded-barcodes-result.html)

### get_recognized_text_lines_result

Gets the recognized text line items from the `CapturedResult`.

```python
def get_recognized_text_lines_result(self) -> "RecognizedTextLinesResult":
```

**Return Value**

Returns a `RecognizedTextLinesResult` object containing the recognized text line items.

**See Also**

[RecognizedTextLinesResult]({{ site.dlr_python_api }}recognized-text-lines-result.html)

### get_detected_quads_result

Gets the detected quads items from the `CapturedResult`.

```python
def get_detected_quads_result(self) -> "DetectedQuadsResult":
```

**Return Value**

Returns a `DetectedQuadsResult` object containing the detected quads items.

**See Also**

[DetectedQuadsResult]({{ site.ddn_python_api }}detected-quads-result.html)

### get_normalized_images_result

Gets the normalized images items from the `CapturedResult`.

```python
def get_normalized_images_result(self) -> "NormalizedImagesResult":
```

**Return Value**

Returns a `NormalizedImagesResult` object containing the normalized images items.

**See Also**

[NormalizedImagesResult]({{ site.ddn_python_api }}normalized-images-result.html)

### get_parsed_result

Gets the parsed result items from the `CapturedResult`.

```python
def get_parsed_result(self) -> "ParsedResult":
```

**Return Value**

Returns a `ParsedResult` object containing the parsed result items.

**See Also**

[ParsedResult]({{ site.dcp_python_api }}parsed-result.html)
