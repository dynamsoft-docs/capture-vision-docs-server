---
layout: default-layout
title: class IntermediateResultReceiver - Dynamsoft Core Module .NET Edition API Reference
description: The class IntermediateResultReceiver of CaptureVisionRouter module .NET Edition is responsible for receiving intermediate results.
keywords: intermediate result receiver, .NET
needAutoGenerateSidebar: true
---

# IntermediateResultReceiver

The `IntermediateResultReceiver` class is responsible for receiving intermediate results of different types. It provides virtual functions for each type of result, which are called when the corresponding result is received.

## Definition

*Namespace:* Dynamsoft.CVR


```csharp
public abstract class IntermediateResultReceiver 
```

## Methods Summary

| Method | Description |
|--------|-------------|
| [`GetObservationParameters`](#getobservationparameters) | Gets the observation parameters of the intermediate result receiver. |
| [`OnTaskResultsReceived`](#ontaskresultsreceived) | Called when a task result has been received. |
| [`OnPredetectedRegionsReceived`](#onpredetectedregionsreceived) | Called when predetected regions have been received. |
| [`OnLocalizedBarcodesReceived`](#onlocalizedbarcodesreceived) | Called when localized barcodes have been received. |
| [`OnDecodedBarcodesReceived`](#ondecodedbarcodesreceived) | Called when decoded barcodes have been received. |
| [`OnLocalizedTextLinesReceived`](#onlocalizedtextlinesreceived) | Called when localized text lines have been received. |
| [`OnRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | Called when recognized text lines have been received. |
| [`OnDetectedQuadsReceived`](#ondetectedquadsreceived) | Called when detected quadrilaterals have been received. |
| [`OnDeskewedImageReceived`](#ondeskewedimagereceived) | Called when deskewed images have been received. |
| [`OnColourImageUnitReceived`](#oncolourimageunitreceived) | Called when colour image units have been received. |
| [`OnScaledColourImageUnitReceived`](#onscaledcolourimageunitreceived) | Called when scaled colour image units have been received. |
| [`OnGrayscaleImageUnitReceived`](#ongrayscaleimageunitreceived) | Called when grayscale image units have been received. |
| [`OnTransformedGrayscaleImageUnitReceived`](#ontransformedgrayscaleimageunitreceived) | Called when transformed grayscale image units have been received. |
| [`OnEnhancedGrayscaleImageUnitReceived`](#onenhancedgrayscaleimageunitreceived) | Called when enhanced grayscale image units have been received. |
| [`OnBinaryImageUnitReceived`](#onbinaryimageunitreceived) | Called when binary image units have been received. |
| [`OnTextureDetectionResultUnitReceived`](#ontexturedetectionresultunitreceived) | Called when texture detection result units have been received. |
| [`OnTextureRemovedGrayscaleImageUnitReceived`](#ontextureremovedgrayscaleimageunitreceived) | Called when texture removed grayscale image units have been received. |
| [`OnTextureRemovedBinaryImageUnitReceived`](#ontextureremovedbinaryimageunitreceived) | Called when texture removed binary image units have been received. |
| [`OnContoursUnitReceived`](#oncontoursunitreceived) | Called when contour units have been received. |
| [`OnLineSegmentsUnitReceived`](#onlinesegmentsunitreceived) | Called when line segment units have been received. |
| [`OnTextZonesUnitReceived`](#ontextzonesunitreceived) | Called when text zone units have been received. |
| [`OnTextRemovedBinaryImageUnitReceived`](#ontextremovedbinaryimageunitreceived) | Called when text removed binary image units have been received. |
| [`OnLongLinesUnitReceived`](#onlonglinesunitreceived) | Called when long line units have been received. |
| [`OnCornersUnitReceived`](#oncornersunitreceived) | Called when corner units have been received. |
| [`OnCandidateQuadEdgesUnitReceived`](#oncandidatequadedgesunitreceived) | Called when candidate quadrilateral edge units have been received. |
| [`OnCandidateBarcodeZonesUnitReceived`](#oncandidatebarcodezonesunitreceived) | Called when candidate barcode zone units have been received. |
| [`OnScaledBarcodeImageUnitReceived`](#onscaledbarcodeimageunitreceived) | Called when scaled barcode image units have been received. |
| [`OnDeformationResistedBarcodeImageUnitReceived`](#ondeformationresistedbarcodeimageunitreceived) | Called when deformation resisted barcode image units have been received. |
| [`OnComplementedBarcodeImageUnitReceived`](#oncomplementedbarcodeimageunitreceived) | Called when complemented barcode image units have been received. |
| [`OnShortLinesUnitReceived`](#onshortlinesunitreceived) | Called when short line units have been received. |
| [`OnRawTextLinesUnitReceived`](#onrawtextlinesunitreceived) | Called when raw text lines have been received. |
| [`OnLogicLinesUnitReceived`](#onlogiclinesunitreceived) | Called when logic lines have been received. |
| [`OnEnhancedImageReceived`](#onenhancedimagereceived) | Called when enhanced images have been received. |
| [`OnTargetROIResultsReceived`](#ontargetroiresultsreceived) | Called when all tasks for the target ROI are completed and the results are deduplicated. |

### GetObservationParameters

Gets the observation parameters of the intermediate result receiver.

```csharp
ObservationParameters GetObservationParameters()
```

**Return value**

Returns the object of `ObservationParameters`. The default parameters are to observe all intermediate result unit types and all tasks.

**See Also**

[ObservationParameters]({{ site.dcvb_dotnet_api }}core/intermediate-results/observed-parameters.html)

### OnTaskResultsReceived

Called when a task result has been received.

```csharp
virtual void OnTaskResultsReceived(IntermediateResult result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The `IntermediateResult` object that contains several result units.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[IntermediateResult]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnPredetectedRegionsReceived

Called when predetected regions have been received.

```csharp
virtual void OnPredetectedRegionsReceived(PredetectedRegionsUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The `PredetectedRegionsUnit` object that contains the result.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[PredetectedRegionsUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/predetected-regions-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnLocalizedBarcodesReceived

Called when localized barcodes have been received.

```csharp
virtual void OnLocalizedBarcodesReceived(LocalizedBarcodesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The `LocalizedBarcodesUnit` object that contains the result.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[LocalizedBarcodesUnit]({{ site.dbr_dotnet_api }}localized-barcodes-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnDecodedBarcodesReceived

Called when decoded barcodes have been received.

```csharp
virtual void OnDecodedBarcodesReceived(DecodedBarcodesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The `DecodedBarcodesUnit` object that contains the result.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[DecodedBarcodesUnit]({{ site.dbr_dotnet_api }}decoded-barcodes-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnLocalizedTextLinesReceived

Called when localized text lines have been received.

```csharp
virtual void OnLocalizedTextLinesReceived(LocalizedTextLinesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The `LocalizedTextLinesUnit` object that contains the result.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[LocalizedTextLinesUnit]({{ site.dlr_dotnet_api }}localized-text-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnRecognizedTextLinesReceived

Called when recognized text lines have been received.

```csharp
virtual void OnRecognizedTextLinesReceived(RecognizedTextLinesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The `RecognizedTextLinesUnit` object that contains the result.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[RecognizedTextLinesUnit]({{ site.dlr_dotnet_api }}recognized-text-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnDetectedQuadsReceived

Called when detected quadrilaterals have been received.

```csharp
virtual void OnDetectedQuadsReceived(DetectedQuadsUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The `DetectedQuadsUnit` object that contains the result.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[DetectedQuadsUnit]({{ site.ddn_dotnet_api }}detected-quads-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnDeskewedImageReceived

Called when deskewed images have been received.

```csharp
virtual void OnDeskewedImageReceived(DeskewedImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The `DeskewedImageUnit` object that contains the result.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[DeskewedImageUnit]({{ site.ddn_dotnet_api }}deskewed-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnColourImageUnitReceived

Called when colour image units have been received.

```csharp
virtual void OnColourImageUnitReceived(ColourImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The received colour image unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[ColourImageUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/colour-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnScaledColourImageUnitReceived

Handles the receipt of a scaled colour image unit.

```csharp
virtual void OnScaledColourImageUnitReceived(ScaledColourImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The received scaled colour image unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[ScaledColourImageUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/scaled-colour-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnGrayscaleImageUnitReceived

Handles the receipt of a grayscale image unit.

```csharp
virtual void OnGrayscaleImageUnitReceived(GrayscaleImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The received grayscale image unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[GrayscaleImageUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/grayscale-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnTransformedGrayscaleImageUnitReceived

Handles the receipt of a transformed grayscale image unit.

```csharp
virtual void OnTransformedGrayscaleImageUnitReceived(TransformedGrayscaleImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The received transformed grayscale image unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[TransformedGrayscaleImageUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/transformed-grayscale-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnEnhancedGrayscaleImageUnitReceived

Handles the receipt of an enhanced grayscale image unit.

```csharp
virtual void OnEnhancedGrayscaleImageUnitReceived(EnhancedGrayscaleImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The received enhanced grayscale image unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[EnhancedGrayscaleImageUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/enhanced-grayscale-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnBinaryImageUnitReceived

Handles the receipt of a binary image unit.

```csharp
virtual void OnBinaryImageUnitReceived(BinaryImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The received binary image unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[BinaryImageUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/binary-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnTextureDetectionResultUnitReceived

Handles the receipt of a texture detection result unit.

```csharp
virtual void OnTextureDetectionResultUnitReceived(TextureDetectionResultUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The received texture detection result unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[TextureDetectionResultUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/texture-detection-result-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnTextureRemovedGrayscaleImageUnitReceived

Handles the receipt of a texture-removed grayscale image unit.

```csharp
virtual void OnTextureRemovedGrayscaleImageUnitReceived(TextureRemovedGrayscaleImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The received texture-removed grayscale image unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[TextureRemovedGrayscaleImageUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/texture-removed-grayscale-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnTextureRemovedBinaryImageUnitReceived

Handles the receipt of a texture-removed binary image unit.

```csharp
virtual void OnTextureRemovedBinaryImageUnitReceived(TextureRemovedBinaryImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The received texture-removed binary image unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[TextureRemovedBinaryImageUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/texture-removed-binary-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnContoursUnitReceived

Handles the receipt of a contours unit.

```csharp
virtual void OnContoursUnitReceived(ContoursUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The contours unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[ContoursUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/contours-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnLineSegmentsUnitReceived

Called when a line segments unit is received.

```csharp
virtual void OnLineSegmentsUnitReceived(LineSegmentsUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The line segments unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[LineSegmentsUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/line-segments-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnTextZonesUnitReceived

Called when a text zones unit is received.

```csharp
virtual void OnTextZonesUnitReceived(TextZonesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The text zones unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[TextZonesUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/text-zones-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnTextRemovedBinaryImageUnitReceived

Called when a text removed binary image unit is received.

```csharp
virtual void OnTextRemovedBinaryImageUnitReceived(TextRemovedBinaryImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The text removed binary image unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[TextRemovedBinaryImageUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/text-removed-binary-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnLongLinesUnitReceived

Called when a long lines unit is received.

```csharp
virtual void OnLongLinesUnitReceived(LongLinesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The long lines unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[LongLinesUnit]({{ site.ddn_dotnet_api }}long-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnCornersUnitReceived

Called when a corners unit is received.

```csharp
virtual void OnCornersUnitReceived(CornersUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The corners unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CornersUnit]({{ site.ddn_dotnet_api }}corners-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnCandidateQuadEdgesUnitReceived

Called when a candidate quad edges unit is received.

```csharp
virtual void OnCandidateQuadEdgesUnitReceived(CandidateQuadEdgesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The candidate quad edges unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CandidateQuadEdgesUnit]({{ site.ddn_dotnet_api }}candidate-quad-edges-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnCandidateBarcodeZonesUnitReceived

Called when a candidate barcode zones unit is received.

```csharp
virtual void OnCandidateBarcodeZonesUnitReceived(CandidateBarcodeZonesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The candidate barcode zones unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CandidateBarcodeZonesUnit]({{ site.dbr_dotnet_api }}candidate-barcode-zones-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnScaledBarcodeImageUnitReceived

Called when a scaled barcode image unit is received.

```csharp
virtual void OnScaledBarcodeImageUnitReceived(ScaledBarcodeImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The scaled barcode image unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[ScaledBarcodeImageUnit]({{ site.dbr_dotnet_api }}scaled-barcode-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnDeformationResistedBarcodeImageUnitReceived

Called when a deformation resisted barcode image unit is received.

```csharp
virtual void OnDeformationResistedBarcodeImageUnitReceived(DeformationResistedBarcodeImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The deformation resisted barcode image unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[DeformationResistedBarcodeImageUnit]({{ site.dbr_dotnet_api }}deformation-resisted-barcode-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnComplementedBarcodeImageUnitReceived

Called when a complemented barcode image unit is received.

```csharp
virtual void OnComplementedBarcodeImageUnitReceived(ComplementedBarcodeImageUnit result，IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The complemented barcode image unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[ComplementedBarcodeImageUnit]({{ site.dbr_dotnet_api }}complemented-barcode-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnShortLinesUnitReceived

Called when short lines units have been received.

```csharp
virtual void OnShortLinesUnitReceived(ShortLinesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The received short lines unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[ShortLinesUnit]({{ site.dcvb_dotnet_api }}core/intermediate-results/short-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnRawTextLinesUnitReceived

Called when raw text lines have been received.

```csharp
virtual void OnRawTextLinesUnitReceived(RawTextLinesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The `RawTextLinesUnit` object that contains the result.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[RawTextLinesUnit]({{ site.dlr_dotnet_api }}raw-text-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnLogicLinesUnitReceived

Called when logic lines have been received.

```csharp
virtual void OnLogicLinesUnitReceived(LogicLinesUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The `LogicLinesUnit` object that contains the result.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[LogicLinesUnit]({{ site.ddn_dotnet_api }}logic-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnEnhancedImageReceived

Called when an enhanced image unit is received.

```csharp
virtual void OnEnhancedImageReceived(EnhancedImageUnit result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The enhanced image unit.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[EnhancedImageUnit]({{ site.ddn_dotnet_api }}enhanced-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)

### OnTargetROIResultsReceived

Called when all tasks for the target ROI are completed and the results are deduplicated.

```csharp
virtual void OnTargetROIResultsReceived(IntermediateResult result, IntermediateResultExtraInfo info)
```

**Parameters**

`[in] result` The `IntermediateResult` object that contains the result.

`[in] info` The `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[IntermediateResult]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result.html)

[IntermediateResultExtraInfo]({{ site.dcvb_dotnet_api }}core/intermediate-results/intermediate-result-extra-info.html)
