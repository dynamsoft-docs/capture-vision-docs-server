---
layout: default-layout
title: class IntermediateResultReceiver - Dynamsoft Core Module Java Edition API Reference
description: The class IntermediateResultReceiver of CaptureVisionRouter module Java Edition is responsible for receiving intermediate results.
keywords: intermediate result receiver, java
needAutoGenerateSidebar: true
---

# IntermediateResultReceiver

The `IntermediateResultReceiver` class is responsible for receiving intermediate results of different types. It provides virtual functions for each type of result, which are called when the corresponding result is received.

## Definition

*Package:* com.dynamsoft.cvr

```java
public class IntermediateResultReceiver 
```

## Methods Summary

| Method | Description |
|--------|-------------|
| [`IntermediateResultReceiver`](#intermediateresultreceiver) | Initializes a new instance of the `IntermediateResultReceiver` class. |
| [`getObservationParameters`](#getobservationparameters) | Gets the observation parameters of the intermediate result receiver. |
| [`onTaskResultsReceived`](#ontaskresultsreceived) | Called when a task result has been received. |
| [`onPredetectedRegionsReceived`](#onpredetectedregionsreceived) | Called when predetected regions have been received. |
| [`onLocalizedBarcodesReceived`](#onlocalizedbarcodesreceived) | Called when localized barcodes have been received. |
| [`onDecodedBarcodesReceived`](#ondecodedbarcodesreceived) | Called when decoded barcodes have been received. |
| [`onLocalizedTextLinesReceived`](#onlocalizedtextlinesreceived) | Called when localized text lines have been received. |
| [`onRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | Called when recognized text lines have been received. |
| [`onDetectedQuadsReceived`](#ondetectedquadsreceived) | Called when detected quadrilaterals have been received. |
| [`onDeskewedImageReceived`](#ondeskewedimagereceived) | Called when deskewed images have been received. |
| [`onEnhancedImageReceived`](#onenhancedimagereceived) | Called when enhanced images have been received. |
| [`onColourImageUnitReceived`](#oncolourimage unitreceived) | Called when colour image units have been received. |
| [`onScaledColourImageUnitReceived`](#onscaledcolourimage unitreceived) | Called when scaled colour image units have been received. |
| [`onGrayscaleImageUnitReceived`](#ongrayscaleimage unitreceived) | Called when grayscale image units have been received. |
| [`onTransformedGrayscaleImageUnitReceived`](#ontransformedgrayscaleimage unitreceived) | Called when transformed grayscale image units have been received. |
| [`onEnhancedGrayscaleImageUnitReceived`](#onenhancedgrayscaleimage unitreceived) | Called when enhanced grayscale image units have been received. |
| [`onBinaryImageUnitReceived`](#onbinaryimage unitreceived) | Called when binary image units have been received. |
| [`onTextureDetectionResultUnitReceived`](#ontexturedetectionresult unitreceived) | Called when texture detection result units have been received. |
| [`onTextureRemovedGrayscaleImageUnitReceived`](#ontextureremovedgrayscaleimage unitreceived) | Called when texture removed grayscale image units have been received. |
| [`onTextureRemovedBinaryImageUnitReceived`](#ontextureremovedbinaryimage unitreceived) | Called when texture removed binary image units have been received. |
| [`onContoursUnitReceived`](#oncontours unitreceived) | Called when contour units have been received. |
| [`onShortLinesUnitReceived`](#onshortlines unitreceived) | Called when short line units have been received. |
| [`onLineSegmentsUnitReceived`](#onlinesegments unitreceived) | Called when line segment units have been received. |
| [`onTextZonesUnitReceived`](#ontextzones unitreceived) | Called when text zone units have been received. |
| [`onTextRemovedBinaryImageUnitReceived`](#ontextremovedbinaryimage unitreceived) | Called when text removed binary image units have been received. |
| [`onLongLinesUnitReceived`](#onlonglines unitreceived) | Called when long line units have been received. |
| [`onCornersUnitReceived`](#oncorners unitreceived) | Called when corner units have been received. |
| [`onCandidateQuadEdgesUnitReceived`](#oncandidatequadedges unitreceived) | Called when candidate quadrilateral edge units have been received. |
| [`onCandidateBarcodeZonesUnitReceived`](#oncandidatebarcodezones unitreceived) | Called when candidate barcode zone units have been received. |
| [`onScaledBarcodeImageUnitReceived`](#onscaledbarcodeimage unitreceived) | Called when scaled barcode image units have been received. |
| [`onDeformationResistedBarcodeImageUnitReceived`](#ondeformationresistedbarcodeimage unitreceived) | Called when deformation resisted barcode image units have been received. |
| [`onComplementedBarcodeImageUnitReceived`](#oncomplementedbarcodeimage unitreceived) | Called when complemented barcode image units have been received. |
| [`onRawTextLinesUnitReceived`](#onrawtextlines unitreceived) | Called when raw text lines have been received. |
| [`onLogicLinesUnitReceived`](#onlogiclines unitreceived) | Called when logic lines have been received. |
| [`onTargetROIResultsReceived`](#ontargetroiresultsreceived) | Called when all tasks for the target ROI are completed and the results are deduplicated. |

### IntermediateResultReceiver

Initializes a new instance of the `IntermediateResultReceiver` class.

```java
public IntermediateResultReceiver()
```

### getObservationParameters

Gets the observation parameters of the intermediate result receiver.

```java
public ObservationParameters getObservationParameters()
```

**Return value**

Returns an `ObservationParameters` object. The default parameters are to observe all intermediate result unit types and all tasks.

**See Also**

[ObservationParameters]({{ site.dcvb_java_api }}core/intermediate-results/observed-parameters.html)

### onTaskResultsReceived

Called when a task result has been received.

```java
public void onTaskResultsReceived(IntermediateResult result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` An `IntermediateResult` object that contains several result units.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[IntermediateResult]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onPredetectedRegionsReceived

Called when predetected regions have been received.

```java
public void onPredetectedRegionsReceived(PredetectedRegionsUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `PredetectedRegionsUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[PredetectedRegionsUnit]({{ site.dcvb_java_api }}core/intermediate-results/predetected-regions-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onLocalizedBarcodesReceived

Called when localized barcodes have been received.

```java
public void onLocalizedBarcodesReceived(LocalizedBarcodesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `LocalizedBarcodesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[LocalizedBarcodesUnit]({{ site.dbr_java_api }}localized-barcodes-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onDecodedBarcodesReceived

Called when decoded barcodes have been received.

```java
public void onDecodedBarcodesReceived(DecodedBarcodesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `DecodedBarcodesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[DecodedBarcodesUnit]({{ site.dbr_java_api }}decoded-barcodes-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onLocalizedTextLinesReceived

Called when localized text lines have been received.

```java
public void onLocalizedTextLinesReceived(LocalizedTextLinesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `LocalizedTextLinesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[LocalizedTextLinesUnit]({{ site.dlr_java_api }}localized-text-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onRecognizedTextLinesReceived

Called when recognized text lines have been received.

```java
public void onRecognizedTextLinesReceived(RecognizedTextLinesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `RecognizedTextLinesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[RecognizedTextLinesUnit]({{ site.dlr_java_api }}recognized-text-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onDetectedQuadsReceived

Called when detected quadrilaterals have been received.

```java
public void onDetectedQuadsReceived(DetectedQuadsUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `DetectedQuadsUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[DetectedQuadsUnit]({{ site.ddn_java_api }}detected-quads-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onDeskewedImageReceived

Called when deskewed images have been received.

```java
public void onDeskewedImageReceived(DeskewedImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `DeskewedImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[DeskewedImageUnit]({{ site.ddn_java_api }}deskewed-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onEnhancedImageReceived

Called when enhanced images have been received.

```java
public void onEnhancedImageReceived(EnhancedImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `EnhancedImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[EnhancedImageUnit]({{ site.ddn_java_api }}enhanced-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onColourImageUnitReceived

Called when colour image units have been received.

```java
public void onColourImageUnitReceived(ColourImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `ColourImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[ColourImageUnit]({{ site.dcvb_java_api }}core/intermediate-results/colour-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onScaledColourImageUnitReceived

Called when scaled colour image units have been received.

```java
public void onScaledColourImageUnitReceived(ScaledColourImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `ScaledColourImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[ScaledColourImageUnit]({{ site.dcvb_java_api }}core/intermediate-results/scaled-colour-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onGrayscaleImageUnitReceived

Called when grayscale image units have been received.

```java
public void onGrayscaleImageUnitReceived(GrayscaleImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `GrayscaleImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[GrayscaleImageUnit]({{ site.dcvb_java_api }}core/intermediate-results/grayscale-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onTransformedGrayscaleImageUnitReceived

Called when transformed grayscale image units have been received.

```java
public void onTransformedGrayscaleImageUnitReceived(TransformedGrayscaleImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `TransformedGrayscaleImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[TransformedGrayscaleImageUnit]({{ site.dcvb_java_api }}core/intermediate-results/transformed-grayscale-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onEnhancedGrayscaleImageUnitReceived

Called when enhanced grayscale image units have been received.

```java
public void onEnhancedGrayscaleImageUnitReceived(EnhancedGrayscaleImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` An `EnhancedGrayscaleImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[EnhancedGrayscaleImageUnit]({{ site.dcvb_java_api }}core/intermediate-results/enhanced-grayscale-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onBinaryImageUnitReceived

Called when binary image units have been received.

```java
public void onBinaryImageUnitReceived(BinaryImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `BinaryImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[BinaryImageUnit]({{ site.dcvb_java_api }}core/intermediate-results/binary-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onTextureDetectionResultUnitReceived

Called when texture detection result units have been received.

```java
public void onTextureDetectionResultUnitReceived(TextureDetectionResultUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `TextureDetectionResultUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[TextureDetectionResultUnit]({{ site.dcvb_java_api }}core/intermediate-results/texture-detection-result-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onTextureRemovedGrayscaleImageUnitReceived

Called when texture-removed grayscale image units have been received.

```java
public void onTextureRemovedGrayscaleImageUnitReceived(TextureRemovedGrayscaleImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `TextureRemovedGrayscaleImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[TextureRemovedGrayscaleImageUnit]({{ site.dcvb_java_api }}core/intermediate-results/texture-removed-grayscale-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onTextureRemovedBinaryImageUnitReceived

Called when texture-removed binary image units have been received.

```java
public void onTextureRemovedBinaryImageUnitReceived(TextureRemovedBinaryImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `TextureRemovedBinaryImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[TextureRemovedBinaryImageUnit]({{ site.dcvb_java_api }}core/intermediate-results/texture-removed-binary-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onContoursUnitReceived

Called when contours units have been received.

```java
public void onContoursUnitReceived(ContoursUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `ContoursUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[ContoursUnit]({{ site.dcvb_java_api }}core/intermediate-results/contours-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onShortLinesUnitReceived

Called when short lines units have been received.

```java
public void onShortLinesUnitReceived(ShortLinesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `ShortLinesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[ShortLinesUnit]({{ site.dcvb_java_api }}core/intermediate-results/short-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onLineSegmentsUnitReceived

Called when a line segments unit is received.

```java
public void onLineSegmentsUnitReceived(LineSegmentsUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `LineSegmentsUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[LineSegmentsUnit]({{ site.dcvb_java_api }}core/intermediate-results/line-segments-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onTextZonesUnitReceived

Called when a text zones unit is received.

```java
public void onTextZonesUnitReceived(TextZonesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `TextZonesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[TextZonesUnit]({{ site.dcvb_java_api }}core/intermediate-results/text-zones-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onTextRemovedBinaryImageUnitReceived

Called when a text removed binary image unit is received.

```java
public void onTextRemovedBinaryImageUnitReceived(TextRemovedBinaryImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `TextRemovedBinaryImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[TextRemovedBinaryImageUnit]({{ site.dcvb_java_api }}core/intermediate-results/text-removed-binary-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onLongLinesUnitReceived

Called when a long lines unit is received.

```java
public void onLongLinesUnitReceived(LongLinesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `LongLinesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[LongLinesUnit]({{ site.ddn_java_api }}long-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onCornersUnitReceived

Called when a corners unit is received.

```java
public void onCornersUnitReceived(CornersUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `CornersUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CornersUnit]({{ site.ddn_java_api }}corners-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onCandidateQuadEdgesUnitReceived

Called when a candidate quad edges unit is received.

```java
public void onCandidateQuadEdgesUnitReceived(CandidateQuadEdgesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `CandidateQuadEdgesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CandidateQuadEdgesUnit]({{ site.ddn_java_api }}candidate-quad-edges-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onCandidateBarcodeZonesUnitReceived

Called when a candidate barcode zones unit is received.

```java
public void onCandidateBarcodeZonesUnitReceived(CandidateBarcodeZonesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `CandidateBarcodeZonesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CandidateBarcodeZonesUnit]({{ site.dbr_java_api }}candidate-barcode-zones-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onScaledBarcodeImageUnitReceived

Called when a scaled barcode image unit is received.

```java
public void onScaledBarcodeImageUnitReceived(ScaledBarcodeImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `ScaledBarcodeImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[ScaledBarcodeImageUnit]({{ site.dbr_java_api }}scaled-barcode-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onDeformationResistedBarcodeImageUnitReceived

Called when a deformation resisted barcode image unit is received.

```java
public void onDeformationResistedBarcodeImageUnitReceived(DeformationResistedBarcodeImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `DeformationResistedBarcodeImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[DeformationResistedBarcodeImageUnit]({{ site.dbr_java_api }}deformation-resisted-barcode-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onComplementedBarcodeImageUnitReceived

Called when a complemented barcode image unit is received.

```java
public void onComplementedBarcodeImageUnitReceived(ComplementedBarcodeImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `ComplementedBarcodeImageUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[ComplementedBarcodeImageUnit]({{ site.dbr_java_api }}complemented-barcode-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onRawTextLinesUnitReceived

Called when raw text lines have been received.

```java
public void onRawTextLinesUnitReceived(RawTextLinesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `RawTextLinesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[RawTextLinesUnit]({{ site.dlr_java_api }}raw-text-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onLogicLinesUnitReceived

Called when logic lines have been received.

```java
public void onLogicLinesUnitReceived(LogicLinesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `LogicLinesUnit` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[LogicLinesUnit]({{ site.ddn_java_api }}logic-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)

### onTargetROIResultsReceived

Called when all tasks for the target ROI are completed and the results are deduplicated.

```java
public void onTargetROIResultsReceived(IntermediateResult result, IntermediateResultExtraInfo info)
```

**Parameters**

`result` A `IntermediateResult` object that contains the result.

`info` An `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[IntermediateResult]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result.html)

[IntermediateResultExtraInfo]({{ site.dcvb_java_api }}core/intermediate-results/intermediate-result-extra-info.html)
