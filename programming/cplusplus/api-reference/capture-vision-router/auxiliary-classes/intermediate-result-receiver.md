---
layout: default-layout
title: class CIntermediateResultReceiver - Dynamsoft Core Module C++ Edition API Reference
description: The class CIntermediateResultReceiver of CaptureVisionRouter module C++ edition is responsible for receiving intermediate results.
keywords: intermediate result receiver, c++
needAutoGenerateSidebar: true
---

# CIntermediateResultReceiver

The `CIntermediateResultReceiver` class is responsible for receiving intermediate results of different types. It provides virtual functions for each type of result, which are called when the corresponding result is received.

## Definition

*Namespace:* dynamsoft::cvr

*Assembly:* DynamsoftCaptureVisionRouter

```cpp
class CIntermediateResultReceiver 
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

```cpp
CObservationParameters* GetObservationParameters()
```

**Return value**

Returns the object of `CObservationParameters`. The default parameters are to observe all intermediate result unit types and all tasks.

**See Also**

[CObservationParameters]({{ site.dcvb_cpp_api }}core/intermediate-results/observed-parameters.html)

### OnTaskResultsReceived

Called when a task result has been received.

```cpp
virtual void OnTaskResultsReceived(CIntermediateResult *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the `CIntermediateResult` object that contains several result units.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CIntermediateResult]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnPredetectedRegionsReceived

Called when predetected regions have been received.

```cpp
virtual void OnPredetectedRegionsReceived(CPredetectedRegionsUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the `CPredetectedRegionsUnit` object that contains the result.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CPredetectedRegionsUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/predetected-regions-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnLocalizedBarcodesReceived

Called when localized barcodes have been received.

```cpp
virtual void OnLocalizedBarcodesReceived(dbr::intermediate_results::CLocalizedBarcodesUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the `CLocalizedBarcodesUnit` object that contains the result.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CLocalizedBarcodesUnit]({{ site.dbr_cpp_api }}localized-barcodes-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnDecodedBarcodesReceived

Called when decoded barcodes have been received.

```cpp
virtual void OnDecodedBarcodesReceived(dbr::intermediate_results::CDecodedBarcodesUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the `CDecodedBarcodesUnit` object that contains the result.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CDecodedBarcodesUnit]({{ site.dbr_cpp_api }}decoded-barcodes-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnLocalizedTextLinesReceived

Called when localized text lines have been received.

```cpp
virtual void OnLocalizedTextLinesReceived(dlr::intermediate_results::CLocalizedTextLinesUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the `CLocalizedTextLinesUnit` object that contains the result.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CLocalizedTextLinesUnit]({{ site.dlr_cpp_api }}localized-text-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnRecognizedTextLinesReceived

Called when recognized text lines have been received.

```cpp
virtual void OnRecognizedTextLinesReceived(dlr::intermediate_results::CRecognizedTextLinesUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the `CRecognizedTextLinesUnit` object that contains the result.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CRecognizedTextLinesUnit]({{ site.dlr_cpp_api }}recognized-text-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnDetectedQuadsReceived

Called when detected quadrilaterals have been received.

```cpp
virtual void OnDetectedQuadsReceived(ddn::intermediate_results::CDetectedQuadsUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the `CDetectedQuadsUnit` object that contains the result.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CDetectedQuadsUnit]({{ site.ddn_cpp_api }}detected-quads-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnDeskewedImageReceived

Called when deskewed images have been received.

```cpp
virtual void OnDeskewedImageReceived(ddn::intermediate_results::CDeskewedImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the `CDeskewedImageUnit` object that contains the result.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CDeskewedImageUnit]({{ site.ddn_cpp_api }}deskewed-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnColourImageUnitReceived

Called when colour image units have been received.

```cpp
virtual void OnColourImageUnitReceived(CColourImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the received colour image unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CColourImageUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/colour-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnScaledColourImageUnitReceived

Handles the receipt of a scaled colour image unit.

```cpp
virtual void OnScaledColourImageUnitReceived(CScaledColourImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the received scaled colour image unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CScaledColourImageUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/scaled-colour-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnGrayscaleImageUnitReceived

Handles the receipt of a grayscale image unit.

```cpp
virtual void OnGrayscaleImageUnitReceived(CGrayscaleImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the received grayscale image unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CGrayscaleImageUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/grayscale-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnTransformedGrayscaleImageUnitReceived

Handles the receipt of a transformed grayscale image unit.

```cpp
virtual void OnTransformedGrayscaleImageUnitReceived(CTransformedGrayscaleImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the received transformed grayscale image unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CTransformedGrayscaleImageUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/transformed-grayscale-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnEnhancedGrayscaleImageUnitReceived

Handles the receipt of an enhanced grayscale image unit.

```cpp
virtual void OnEnhancedGrayscaleImageUnitReceived(CEnhancedGrayscaleImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the received enhanced grayscale image unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CEnhancedGrayscaleImageUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/enhanced-grayscale-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnBinaryImageUnitReceived

Handles the receipt of a binary image unit.

```cpp
virtual void OnBinaryImageUnitReceived(CBinaryImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the received binary image unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CBinaryImageUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/binary-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnTextureDetectionResultUnitReceived

Handles the receipt of a texture detection result unit.

```cpp
virtual void OnTextureDetectionResultUnitReceived(CTextureDetectionResultUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the received texture detection result unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CTextureDetectionResultUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/texture-detection-result-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnTextureRemovedGrayscaleImageUnitReceived

Handles the receipt of a texture-removed grayscale image unit.

```cpp
virtual void OnTextureRemovedGrayscaleImageUnitReceived(CTextureRemovedGrayscaleImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the received texture-removed grayscale image unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CTextureRemovedGrayscaleImageUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/texture-removed-grayscale-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnTextureRemovedBinaryImageUnitReceived

Handles the receipt of a texture-removed binary image unit.

```cpp
virtual void OnTextureRemovedBinaryImageUnitReceived(CTextureRemovedBinaryImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the received texture-removed binary image unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CTextureRemovedBinaryImageUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/texture-removed-binary-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnContoursUnitReceived

Handles the receipt of a contours unit.

```cpp
virtual void OnContoursUnitReceived(CContoursUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the contours unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CContoursUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/contours-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnLineSegmentsUnitReceived

Called when a line segments unit is received.

```cpp
virtual void OnLineSegmentsUnitReceived(CLineSegmentsUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the line segments unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CLineSegmentsUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/line-segments-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnTextZonesUnitReceived

Called when a text zones unit is received.

```cpp
virtual void OnTextZonesUnitReceived(CTextZonesUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the text zones unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CTextZonesUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/text-zones-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnTextRemovedBinaryImageUnitReceived

Called when a text removed binary image unit is received.

```cpp
virtual void OnTextRemovedBinaryImageUnitReceived(CTextRemovedBinaryImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the text removed binary image unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CTextRemovedBinaryImageUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/text-removed-binary-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnLongLinesUnitReceived

Called when a long lines unit is received.

```cpp
virtual void OnLongLinesUnitReceived(ddn::intermediate_results::CLongLinesUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the long lines unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CLongLinesUnit]({{ site.ddn_cpp_api }}long-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnCornersUnitReceived

Called when a corners unit is received.

```cpp
virtual void OnCornersUnitReceived(ddn::intermediate_results::CCornersUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the corners unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CCornersUnit]({{ site.ddn_cpp_api }}corners-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnCandidateQuadEdgesUnitReceived

Called when a candidate quad edges unit is received.

```cpp
virtual void OnCandidateQuadEdgesUnitReceived(ddn::intermediate_results::CCandidateQuadEdgesUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the candidate quad edges unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CCandidateQuadEdgesUnit]({{ site.ddn_cpp_api }}candidate-quad-edges-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnCandidateBarcodeZonesUnitReceived

Called when a candidate barcode zones unit is received.

```cpp
virtual void OnCandidateBarcodeZonesUnitReceived(dbr::intermediate_results::CCandidateBarcodeZonesUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the candidate barcode zones unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CCandidateBarcodeZonesUnit]({{ site.dbr_cpp_api }}candidate-barcode-zones-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnScaledBarcodeImageUnitReceived

Called when a scaled barcode image unit is received.

```cpp
virtual void OnScaledBarcodeImageUnitReceived(dbr::intermediate_results::CScaledBarcodeImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the scaled barcode image unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CScaledBarcodeImageUnit]({{ site.dbr_cpp_api }}scaled-barcode-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnDeformationResistedBarcodeImageUnitReceived

Called when a deformation resisted barcode image unit is received.

```cpp
virtual void OnDeformationResistedBarcodeImageUnitReceived(dbr::intermediate_results::CDeformationResistedBarcodeImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the deformation resisted barcode image unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CDeformationResistedBarcodeImageUnit]({{ site.dbr_cpp_api }}deformation-resisted-barcode-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnComplementedBarcodeImageUnitReceived

Called when a complemented barcode image unit is received.

```cpp
virtual void OnComplementedBarcodeImageUnitReceived(dbr::intermediate_results::CComplementedBarcodeImageUnit *pResult，const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the complemented barcode image unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CComplementedBarcodeImageUnit]({{ site.dbr_cpp_api }}complemented-barcode-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnShortLinesUnitReceived

Called when short lines units have been received.

```cpp
virtual void OnShortLinesUnitReceived(CShortLinesUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the received short lines unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CShortLinesUnit]({{ site.dcvb_cpp_api }}core/intermediate-results/short-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnRawTextLinesUnitReceived

Called when raw text lines have been received.

```cpp
virtual void OnRawTextLinesUnitReceived(dlr::intermediate_results::CRawTextLinesUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the `CRawTextLinesUnit` object that contains the result.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CRawTextLinesUnit]({{ site.dlr_cpp_api }}raw-text-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnLogicLinesUnitReceived

Called when logic lines have been received.

```cpp
virtual void OnLogicLinesUnitReceived(ddn::intermediate_results::CLogicLinesUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the `CLogicLinesUnit` object that contains the result.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CLogicLinesUnit]({{ site.ddn_cpp_api }}logic-lines-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnEnhancedImageReceived

Called when an enhanced image unit is received.

```cpp
virtual void OnEnhancedImageReceived(ddn::intermediate_results::CEnhancedImageUnit *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the enhanced image unit.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CEnhancedImageUnit]({{ site.ddn_cpp_api }}enhanced-image-unit.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)

### OnTargetROIResultsReceived

Called when all tasks for the target ROI are completed and the results are deduplicated.

```cpp
virtual void OnTargetROIResultsReceived(CIntermediateResult *pResult, const IntermediateResultExtraInfo* info)
```

**Parameters**

`[in] pResult` A pointer to the `CIntermediateResult` object that contains the result.

`[in] info` A pointer to the `IntermediateResultExtraInfo` object that contains the extra info of intermediate result.

**See Also**

[CIntermediateResult]({{ site.dcvb_cpp_api }}core/intermediate-results/intermediate-result.html)

[IntermediateResultExtraInfo]({{ site.dcvb_cpp_api }}core/structs/intermediate-result-extra-info.html)
