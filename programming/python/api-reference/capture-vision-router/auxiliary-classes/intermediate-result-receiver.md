---
layout: default-layout
title: class IntermediateResultReceiver - Dynamsoft Core Module Python Edition API Reference
description: The class IntermediateResultReceiver of CaptureVisionRouter module Python Edition is responsible for receiving intermediate results.
keywords: intermediate result receiver, python
needAutoGenerateSidebar: true
---

# IntermediateResultReceiver

The `IntermediateResultReceiver` class is responsible for receiving intermediate results of different types. It provides virtual functions for each type of result, which are called when the corresponding result is received.

## Definition

*Module:* dynamsoft_capture_vision_router

```python
class IntermediateResultReceiver(AbstractIntermediateResultReceiver) 
```

## Methods Summary

| Method | Description |
|--------|-------------|
| [`__init__`](#__init__) | Initializes a new instance of the `IntermediateResultReceiver` class. |
| [`get_observation_parameters`](#get_observation_parameters) | Gets the observation parameters of the intermediate result receiver. |
| [`on_task_results_received`](#on_task_results_received) | Called when a task result has been received. |
| [`on_predetected_regions_received`](#on_predetected_regions_received) | Called when predetected regions have been received. |
| [`on_localized_barcodes_received`](#on_localized_barcodes_received) | Called when localized barcodes have been received. |
| [`on_decoded_barcodes_received`](#on_decoded_barcodes_received) | Called when decoded barcodes have been received. |
| [`on_localized_text_lines_received`](#on_localized_text_lines_received) | Called when localized text lines have been received. |
| [`on_recognized_text_lines_received`](#on_recognized_text_lines_received) | Called when recognized text lines have been received. |
| [`on_detected_quads_received`](#on_detected_quads_received) | Called when detected quadrilaterals have been received. |
| [`on_deskewed_image_received`](#on_deskewed_image_received) | Called when deskewed images have been received. |
| [`on_enhanced_image_received`](#on_enhanced_image_received) | Called when enhanced images have been received. |
| [`on_colour_image_unit_received`](#on_colour_image_unit_received) | Called when colour image units have been received. |
| [`on_scaled_colour_image_unit_received`](#on_scaled_colour_image_unit_received) | Called when scaled colour image units have been received. |
| [`on_grayscale_image_unit_received`](#on_grayscale_image_unit_received) | Called when grayscale image units have been received. |
| [`on_transformed_grayscale_image_unit_received`](#on_transformed_grayscale_image_unit_received) | Called when transformed grayscale image units have been received. |
| [`on_enhanced_grayscale_image_unit_received`](#on_enhanced_grayscale_image_unit_received) | Called when enhanced grayscale image units have been received. |
| [`on_binary_image_unit_received`](#on_binary_image_unit_received) | Called when binary image units have been received. |
| [`on_texture_detection_result_unit_received`](#on_texture_detection_result_unit_received) | Called when texture detection result units have been received. |
| [`on_texture_removed_grayscale_image_unit_received`](#on_texture_removed_grayscale_image_unit_received) | Called when texture removed grayscale image units have been received. |
| [`on_texture_removed_binary_image_unit_received`](#on_texture_removed_binary_image_unit_received) | Called when texture removed binary image units have been received. |
| [`on_contours_unit_received`](#on_contours_unit_received) | Called when contour units have been received. |
| [`on_line_segments_unit_received`](#on_line_segments_unit_received) | Called when line segment units have been received. |
| [`on_text_zones_unit_received`](#on_text_zones_unit_received) | Called when text zone units have been received. |
| [`on_text_removed_binary_image_unit_received`](#on_text_removed_binary_image_unit_received) | Called when text removed binary image units have been received. |
| [`on_long_lines_unit_received`](#on_long_lines_unit_received) | Called when long line units have been received. |
| [`on_corners_unit_received`](#on_corners_unit_received) | Called when corner units have been received. |
| [`on_candidate_quad_edges_unit_received`](#on_candidate_quad_edges_unit_received) | Called when candidate quadrilateral edge units have been received. |
| [`on_candidate_barcode_zones_unit_received`](#on_candidate_barcode_zones_unit_received) | Called when candidate barcode zone units have been received. |
| [`on_scaled_barcode_image_unit_received`](#on_scaled_barcode_image_unit_received) | Called when scaled barcode image units have been received. |
| [`on_deformation_resisted_barcode_image_unit_received`](#on_deformation_resisted_barcode_image_unit_received) | Called when deformation resisted barcode image units have been received. |
| [`on_complemented_barcode_image_unit_received`](#on_complemented_barcode_image_unit_received) | Called when complemented barcode image units have been received. |
| [`on_short_lines_unit_received`](#on_short_lines_unit_received) | Called when short line units have been received. |
| [`on_raw_text_lines_unit_received`](#on_raw_text_lines_unit_received) | Called when raw text lines have been received. |
| [`on_logic_lines_unit_received`](#on_logic_lines_unit_received) | Called when logic lines have been received. |
| [`on_target_roi_results_received`](#on_target_roi_results_received) | Called when all tasks for the target ROI are completed and the results are deduplicated. |

### \_\_init\_\_

Initializes a new instance of the `IntermediateResultReceiver` class.

```python
def __init__(self):
```

### get_observation_parameters

Gets the observation parameters of the intermediate result receiver.

```python
def get_observation_parameters(self) -> ObservationParameters:
```

**Return value**

Returns an `ObservationParameters` object. The default parameters are to observe all intermediate result unit types and all tasks.

**See Also**

[ObservationParameters]({{ site.dcvb_python_api }}core/intermediate-results/observed-parameters.html)

### on_task_results_received

Called when a task result has been received.

```python
def on_task_results_received(self, result: IntermediateResult, info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` An `IntermediateResult` object that contains several result units.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[IntermediateResult]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_predetected_regions_received

Called when predetected regions have been received.

```python
def on_predetected_regions_received(self, result: PredetectedRegionsUnit, info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `PredetectedRegionsUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[PredetectedRegionsUnit]({{ site.dcvb_python_api }}core/intermediate-results/predetected-regions-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_localized_barcodes_received

Called when localized barcodes have been received.

```python
def on_localized_barcodes_received(self, result: "LocalizedBarcodesUnit", info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `LocalizedBarcodesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[LocalizedBarcodesUnit]({{ site.dbr_python_api }}localized-barcodes-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_decoded_barcodes_received

Called when decoded barcodes have been received.

```python
def on_decoded_barcodes_received(self, result: "DecodedBarcodesUnit", info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `DecodedBarcodesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[DecodedBarcodesUnit]({{ site.dbr_python_api }}decoded-barcodes-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_localized_text_lines_received

Called when localized text lines have been received.

```python
def on_localized_text_lines_received(self, result: "LocalizedTextLinesUnit", info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `LocalizedTextLinesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[LocalizedTextLinesUnit]({{ site.dlr_python_api }}localized-text-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_recognized_text_lines_received

Called when recognized text lines have been received.

```python
def on_recognized_text_lines_received(self, result: "RecognizedTextLinesUnit", info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `RecognizedTextLinesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[RecognizedTextLinesUnit]({{ site.dlr_python_api }}recognized-text-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_detected_quads_received

Called when detected quadrilaterals have been received.

```python
def on_detected_quads_received(self, result: "DetectedQuadsUnit", info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `DetectedQuadsUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[DetectedQuadsUnit]({{ site.ddn_python_api }}detected-quads-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_deskewed_image_received

Called when deskewed images have been received.

```python
def on_deskewed_image_received(self, result: "DeskewedImageUnit", info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `DeskewedImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[DeskewedImageUnit]({{ site.ddn_python_api }}deskewed-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_enhanced_image_received

Called when enhanced images have been received.

```python
def on_enhanced_image_received(self, result: "EnhancedImageUnit", info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `EnhancedImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[EnhancedImageUnit]({{ site.ddn_python_api }}enhanced-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_colour_image_unit_received

Called when colour image units have been received.

```python
def on_colour_image_unit_received(self, result: ColourImageUnit, info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `ColourImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[ColourImageUnit]({{ site.dcvb_python_api }}core/intermediate-results/colour-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_scaled_colour_image_unit_received

Called when scaled colour image units have been received.

```python
def on_scaled_colour_image_unit_received(self, result: ScaledColourImageUnit, info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `ScaledColourImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[ScaledColourImageUnit]({{ site.dcvb_python_api }}core/intermediate-results/scaled-colour-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_grayscale_image_unit_received

Called when grayscale image units have been received.

```python
def on_grayscale_image_unit_received(self, result: GrayscaleImageUnit, info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `GrayscaleImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[GrayscaleImageUnit]({{ site.dcvb_python_api }}core/intermediate-results/grayscale-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_transformed_grayscale_image_unit_received

Called when transformed grayscale image units have been received.

```python
def on_transformed_grayscale_image_unit_received(self, result: TransformedGrayscaleImageUnit, info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `TransformedGrayscaleImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[TransformedGrayscaleImageUnit]({{ site.dcvb_python_api }}core/intermediate-results/transformed-grayscale-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_enhanced_grayscale_image_unit_received

Called when enhanced grayscale image units have been received.

```python
def on_enhanced_grayscale_image_unit_received(self, result: EnhancedGrayscaleImageUnit, info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` An `EnhancedGrayscaleImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[EnhancedGrayscaleImageUnit]({{ site.dcvb_python_api }}core/intermediate-results/enhanced-grayscale-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_binary_image_unit_received

Called when binary image units have been received.

```python
def on_binary_image_unit_received(self, result: BinaryImageUnit, info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `BinaryImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[BinaryImageUnit]({{ site.dcvb_python_api }}core/intermediate-results/binary-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_texture_detection_result_unit_received

Called when texture detection result units have been received.

```python
def on_texture_detection_result_unit_received(self, result: TextureDetectionResultUnit, info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `TextureDetectionResultUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[TextureDetectionResultUnit]({{ site.dcvb_python_api }}core/intermediate-results/texture-detection-result-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_texture_removed_grayscale_image_unit_received

Called when texture-removed grayscale image units have been received.

```python
def on_texture_removed_grayscale_image_unit_received(self, result: TextureRemovedGrayscaleImageUnit, info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `TextureRemovedGrayscaleImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[TextureRemovedGrayscaleImageUnit]({{ site.dcvb_python_api }}core/intermediate-results/texture-removed-grayscale-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_texture_removed_binary_image_unit_received

Called when texture-removed binary image units have been received.

```python
def on_texture_removed_binary_image_unit_received(self, result: TextureRemovedBinaryImageUnit, info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `TextureRemovedBinaryImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[TextureRemovedBinaryImageUnit]({{ site.dcvb_python_api }}core/intermediate-results/texture-removed-binary-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_contours_unit_received

Called when contours units have been received.

```python
def on_contours_unit_received(self, result: ContoursUnit, info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `ContoursUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[ContoursUnit]({{ site.dcvb_python_api }}core/intermediate-results/contours-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_line_segments_unit_received

Called when a line segments unit is received.

```python
def on_line_segments_unit_received(self, result: LineSegmentsUnit, info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `LineSegmentsUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[LineSegmentsUnit]({{ site.dcvb_python_api }}core/intermediate-results/line-segments-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_text_zones_unit_received

Called when a text zones unit is received.

```python
def on_text_zones_unit_received(self, result: TextZonesUnit, info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `TextZonesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[TextZonesUnit]({{ site.dcvb_python_api }}core/intermediate-results/text-zones-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_text_removed_binary_image_unit_received

Called when a text removed binary image unit is received.

```python
def on_text_removed_binary_image_unit_received(self, result: TextRemovedBinaryImageUnit, info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `TextRemovedBinaryImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[TextRemovedBinaryImageUnit]({{ site.dcvb_python_api }}core/intermediate-results/text-removed-binary-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_long_lines_unit_received

Called when a long lines unit is received.

```python
def on_long_lines_unit_received(self, result: "LongLinesUnit", info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `LongLinesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[LongLinesUnit]({{ site.ddn_python_api }}long-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_corners_unit_received

Called when a corners unit is received.

```python
def on_corners_unit_received(self, result: "CornersUnit", info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `CornersUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CornersUnit]({{ site.ddn_python_api }}corners-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_candidate_quad_edges_unit_received

Called when a candidate quad edges unit is received.

```python
def on_candidate_quad_edges_unit_received(self, result: "CandidateQuadEdgesUnit", info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `CandidateQuadEdgesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CandidateQuadEdgesUnit]({{ site.ddn_python_api }}candidate-quad-edges-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_candidate_barcode_zones_unit_received

Called when a candidate barcode zones unit is received.

```python
def on_candidate_barcode_zones_unit_received(self, result: "CandidateBarcodeZonesUnit", info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `CandidateBarcodeZonesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CandidateBarcodeZonesUnit]({{ site.dbr_python_api }}candidate-barcode-zones-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_scaled_barcode_image_unit_received

Called when a scaled barcode image unit is received.

```python
def on_scaled_barcode_image_unit_received(self, result: "ScaledBarcodeImageUnit", info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `ScaledBarcodeImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[ScaledBarcodeImageUnit]({{ site.dbr_python_api }}scaled-barcode-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_deformation_resisted_barcode_image_unit_received

Called when a deformation resisted barcode image unit is received.

```python
def on_deformation_resisted_barcode_image_unit_received(self, result: "DeformationResistedBarcodeImageUnit", info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `DeformationResistedBarcodeImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[DeformationResistedBarcodeImageUnit]({{ site.dbr_python_api }}deformation-resisted-barcode-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_complemented_barcode_image_unit_received

Called when a complemented barcode image unit is received.

```python
def on_complemented_barcode_image_unit_received(self, result: "ComplementedBarcodeImageUnit", info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `ComplementedBarcodeImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[ComplementedBarcodeImageUnit]({{ site.dbr_python_api }}complemented-barcode-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_short_lines_unit_received

Called when short lines units have been received.

```python
def on_short_lines_unit_received(self, result: ShortLinesUnit, info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `ShortLinesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[ShortLinesUnit]({{ site.dcvb_python_api }}core/intermediate-results/short-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_raw_text_lines_unit_received

Called when raw text lines have been received.

```python
def on_raw_text_lines_unit_received(self, result: "RawTextLinesUnit", info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `RawTextLinesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[RawTextLinesUnit]({{ site.dlr_python_api }}raw-text-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_logic_lines_unit_received

Called when logic lines have been received.

```python
def on_logic_lines_unit_received(self, result: "LogicLinesUnit", info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `LogicLinesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[LogicLinesUnit]({{ site.ddn_python_api }}logic-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

### on_target_roi_results_received

Called when raw text lines have been received.

```python
def on_target_roi_results_received(self, result: IntermediateResult, info: IntermediateResultExtraInfo) -> None:
```

**Parameters**

`result` A `IntermediateResult` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[IntermediateResult]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result.html)

[IntermediateResultExtraInfo]({{ site.dcvb_python_api }}core/intermediate-results/intermediate-result-extra-info.html)

