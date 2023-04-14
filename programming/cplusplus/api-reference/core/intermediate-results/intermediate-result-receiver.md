---
layout: default-layout
title: class CIntermediateResultReceiver - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CIntermediateResultReceiver in Dynamsoft Core Module.
keywords: intermediate result receiver, c++
needAutoGenerateSidebar: true
---

# CIntermediateResultReceiver

The CIntermediateResultReceiver class is responsible for receiving intermediate results of different types. It provides virtual functions for each type of result, which are called when the corresponding result is received.

```cpp
class dynamsoft::intermediate_results::CIntermediateResultReceiver 
```

---

## Methods Summary

| Method | Description |
|--------|-------------|
| [`GetObservedResultUnitTypes`](#getobservedresultunittypes) | Gets the types of intermediate result units that have been observed. |
| [`GetResultLevel`](#getresultlevel) | Gets the result generation level of the intermediate result receiver. |
| [`OnPredetectedRegionsReceived`](#onpredetectedregionsreceived) | Called when predetected regions have been received. |
| [`OnLocalizedBarcodesReceived`](#onlocalizedbarcodesreceived) | Called when localized barcodes have been received. |
| [`OnDecodedBarcodesReceived`](#ondecodedbarcodesreceived) | Called when decoded barcodes have been received. |
| [`OnLocalizedTextLinesReceived`](#onlocalizedtextlinesreceived) | Called when localized text lines have been received. |
| [`OnRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | Called when recognized text lines have been received. |
| [`OnDetectedQuadsReceived`](#ondetectedquadsreceived) | Called when detected quadrilaterals have been received. |
| [`OnNormalizedImagesReceived`](#onnormalizedimagesreceived) | Called when normalized images have been received. |
| [`OnColourImageUnitReceived`](#oncolourimageunitreceived) | Called when colour image units have been received. |
| [`OnScaledDownColourImageUnitReceived`](#onscaleddowncolourimageunitreceived) | Called when scaled down colour image units have been received. |
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
| [`OnScaledUpBarcodeImageUnitReceived`](#onscaledupbarcodeimageunitreceived) | Called when scaled up barcode image units have been received. |
| [`OnDeformationResistedBarcodeImageUnitReceived`](#ondeformationresistedbarcodeimageunitreceived) | Called when deformation resisted barcode image units have been received. |
| [`OnComplementedBarcodeImageUnitReceived`](#oncomplementedbarcodeimageunitreceived) | Called when complemented barcode image units have been received. |

### GetObservedResultUnitTypes

Gets the types of intermediate result units that have been observed.

```cpp
unsigned long long GetObservedResultUnitTypes()
```

**Return value**

Returns a bit mask of the intermediate result unit types that have been observed.

### GetResultLevel

Gets the result generation level of the intermediate result receiver.

```cpp
int GetResultLevel()
```

**Return value**

Returns the result generation level of the intermediate result receiver.

### OnPredetectedRegionsReceived

Called when predetected regions have been received.

```cpp
virtual void OnPredetectedRegionsReceived(const char* targetROIDefName, 
                                          const char* taskName, 
                                          const CPredetectedRegionsUnit *pResult)
```

**Parameters**

`[in] targetROIDefName` The name of the target region of interest definition.

`[in] taskName` The name of the task that produced the result.

`[in] pResult` A pointer to the CPredetectedRegionsUnit object that contains the result.

### OnLocalizedBarcodesReceived

Called when localized barcodes have been received.

```cpp
virtual void OnLocalizedBarcodesReceived(const char* targetROIDefName, 
                                          const char* taskName, 
                                          const dbr::intermediate_results::CLocalizedBarcodesUnit *pResult)
```

**Parameters**

`[in] targetROIDefName` The name of the target region of interest definition.

`[in] taskName` The name of the task that produced the result.

`[in] pResult` A pointer to the CLocalizedBarcodesUnit object that contains the result.

### OnDecodedBarcodesReceived

Called when decoded barcodes have been received.

```cpp
virtual void OnDecodedBarcodesReceived(const char* targetROIDefName, 
                                          const char* taskName, 
                                          const dbr::intermediate_results::CDecodedBarcodesUnit *pResult)
```

**Parameters**

`[in] targetROIDefName` The name of the target region of interest definition.

`[in] taskName` The name of the task that produced the result.

`[in] pResult` A pointer to the CDecodedBarcodesUnit object that contains the result.

### OnLocalizedTextLinesReceived

Called when localized text lines have been received.

```cpp
virtual void OnLocalizedTextLinesReceived(const char* targetROIDefName, 
                                          const char* taskName, 
                                          const dlr::intermediate_results::CLocalizedTextLinesUnit *pResult)
```

**Parameters**

`[in] targetROIDefName` The name of the target region of interest definition.

`[in] taskName` The name of the task that produced the result.

`[in] pResult` A pointer to the CLocalizedTextLinesUnit object that contains the result.

### OnRecognizedTextLinesReceived

Called when recognized text lines have been received.

```cpp
virtual void OnRecognizedTextLinesReceived(const char* targetROIDefName, 
                                          const char* taskName, 
                                          const dlr::intermediate_results::CRecognizedTextLinesUnit *pResult)
```

**Parameters**

`[in] targetROIDefName` The name of the target region of interest definition.

`[in] taskName` The name of the task that produced the result.

`[in] pResult` A pointer to the CRecognizedTextLinesUnit object that contains the result.

### OnDetectedQuadsReceived

Called when detected quadrilaterals have been received.

```cpp
virtual void OnDetectedQuadsReceived(const char* targetROIDefName, 
                                          const char* taskName, 
                                          const ddn::intermediate_results::CDetectedQuadsUnit *pResult)
```

**Parameters**

`[in] targetROIDefName` The name of the target region of interest definition.

`[in] taskName` The name of the task that produced the result.

`[in] pResult` A pointer to the CDetectedQuadsUnit object that contains the result.

### OnNormalizedImagesReceived

Called when normalized images have been received.

```cpp
virtual void OnNormalizedImagesReceived(const char* targetROIDefName, 
                                          const char* taskName, 
                                          const ddn::intermediate_results::CNormalizedImageUnit *pResult)
```

**Parameters**

`[in] targetROIDefName` The name of the target region of interest definition.

`[in] taskName` The name of the task that produced the result.

`[in] pResult` A pointer to the CNormalizedImageUnit object that contains the result.

### OnColourImageUnitReceived

Called when colour image units have been received.

```cpp
virtual void OnColourImageUnitReceived(const char* targetROIDefName, 
                                          const char* taskName, 
                                          SectionType sectionType, 
                                          const CColourImageUnit *pResult)
```

**Parameters**

`[in] targetROIDefName` The name of the target region of interest definition.

`[in] taskName` The name of the task that produced the result.

`[in] sectionType` The section type of the result.

`[in] pResult` A pointer to the received colour image unit.

### OnScaledDownColourImageUnitReceived

Handles the receipt of a scaled-down colour image unit.

```cpp
virtual void OnScaledDownColourImageUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    SectionType sectionType, 
                                                    const CScaledDownColourImageUnit *pResult);
```

**Parameters**

`[in] targetROIDefName` The name of the target ROI definition.

`[in] taskName` The name of the task that produced the result.

`[in] sectionType` The section type of the result.

`[in] pResult` A pointer to the received scaled-down colour image unit.

### OnGrayscaleImageUnitReceived

Handles the receipt of a grayscale image unit.

```cpp
virtual void OnGrayscaleImageUnitReceived(const char* targetROIDefName, 
                                            const char* taskName, 
                                            SectionType sectionType, 
                                            const CGrayscaleImageUnit *pResult);
```

**Parameters**

`[in] targetROIDefName` The name of the target ROI definition.

`[in] taskName` The name of the task that produced the result.

`[in] sectionType` The section type of the result.

`[in] pResult` A pointer to the received grayscale image unit.

### OnTransformedGrayscaleImageUnitReceived

Handles the receipt of a transformed grayscale image unit.

```cpp
virtual void OnTransformedGrayscaleImageUnitReceived(const char* targetROIDefName, 
                                                        const char* taskName, 
                                                        SectionType sectionType, 
                                                        const CTransformedGrayscaleImageUnit *pResult);
```

**Parameters**

`[in] targetROIDefName` The name of the target ROI definition.

`[in] taskName` The name of the task that produced the result.

`[in] sectionType` The section type of the result.

`[in] pResult` A pointer to the received transformed grayscale image unit.

### OnEnhancedGrayscaleImageUnitReceived

Handles the receipt of an enhanced grayscale image unit.

```cpp
virtual void OnEnhancedGrayscaleImageUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    SectionType sectionType, 
                                                    const CEnhancedGrayscaleImageUnit *pResult);
```

**Parameters**

`[in] targetROIDefName` The name of the target ROI definition.

`[in] taskName` The name of the task that produced the result.

`[in] sectionType` The section type of the result.

`[in] pResult` A pointer to the received enhanced grayscale image unit.

### OnBinaryImageUnitReceived

Handles the receipt of a binary image unit.

```cpp
virtual void OnBinaryImageUnitReceived(const char* targetROIDefName, 
                                        const char* taskName, 
                                        SectionType sectionType, 
                                        const CBinaryImageUnit *pResult);
```

**Parameters**

`[in] targetROIDefName` The name of the target ROI definition.

`[in] taskName` The name of the task that produced the result.

`[in] sectionType` The section type of the result.

`[in] pResult` A pointer to the received binary image unit.

### OnTextureDetectionResultUnitReceived

Handles the receipt of a texture detection result unit.

```cpp
virtual void OnTextureDetectionResultUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    SectionType sectionType, 
                                                    const CTextureDetectionResultUnit *pResult);
```

**Parameters**

`[in] targetROIDefName` The name of the target ROI definition.

`[in] taskName` The name of the task that produced the result.

`[in] sectionType` The section type of the result.

`[in] pResult` A pointer to the received texture detection result unit.

### OnTextureRemovedGrayscaleImageUnitReceived

Handles the receipt of a texture-removed grayscale image unit.

```cpp
virtual void OnTextureRemovedGrayscaleImageUnitReceived(const char* targetROIDefName, 
                                                        const char* taskName, 
                                                        SectionType sectionType, 
                                                        const CTextureRemovedGrayscaleImageUnit *pResult);
```

**Parameters**

`[in] targetROIDefName` The name of the target ROI definition.

`[in] taskName` The name of the task that produced the result.

`[in] sectionType` The section type of the result.

`[in] pResult` A pointer to the received texture-removed grayscale image unit.

### OnTextureRemovedBinaryImageUnitReceived

Handles the receipt of a texture-removed binary image unit.

```cpp
virtual void OnTextureRemovedBinaryImageUnitReceived(const char* targetROIDefName, 
                                                        const char* taskName, 
                                                        SectionType sectionType, 
                                                        const CTextureRemovedBinaryImageUnit *pResult);
```

**Parameters**

`[in] targetROIDefName` The name of the target ROI definition.

`[in] taskName` The name of the task that produced the result.

`[in] sectionType` The section type of the result.

`[in] pResult` A pointer to the received texture-removed binary image unit.

### OnContoursUnitReceived

Handles the receipt of a contours unit.

```cpp
virtual void OnContoursUnitReceived(const char* targetROIDefName, 
                                    const char* taskName, 
                                    SectionType sectionType, 
                                    const CContoursUnit *pResult);
```

**Parameters**

`[in] targetROIDefName` The name of the target ROI definition.

`[in] taskName` The name of the task that produced the result.

`[in] sectionType` The section type of the result.

`[in] pResult` A pointer to the contours unit.

### OnLineSegmentsUnitReceived

Called when a line segments unit is received.

```cpp
virtual void OnLineSegmentsUnitReceived(const char* targetROIDefName, 
                                        const char* taskName, 
                                        SectionType sectionType, 
                                        const CLineSegmentsUnit *pResult)
```

**Parameters**

`[in] targetROIDefName` The name of the target ROI definition.

`[in] taskName` The name of the task that produced the result.

`[in] sectionType` The section type of the result.

`[in] pResult` A pointer to the line segments unit.

### OnTextZonesUnitReceived

Called when a text zones unit is received.

```cpp
virtual void OnTextZonesUnitReceived(const char* targetROIDefName, 
                                        const char* taskName, 
                                        SectionType sectionType, 
                                        const CTextZonesUnit *pResult)
```

**Parameters**

`[in] targetROIDefName` The name of the target ROI definition.

`[in] taskName` The name of the task that produced the result.

`[in] sectionType` The section type of the result.

`[in] pResult` A pointer to the text zones unit.

### OnTextRemovedBinaryImageUnitReceived

Called when a text removed binary image unit is received.

```cpp
virtual void OnTextRemovedBinaryImageUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    SectionType sectionType,
                                                    const CTextRemovedBinaryImageUnit *pResult)
```

**Parameters**

`[in] targetROIDefName` The name of the target ROI definition.

`[in] taskName` The name of the task that produced the result.

`[in] sectionType` The section type of the result.

`[in] pResult` A pointer to the text removed binary image unit.

### OnLongLinesUnitReceived

Called when a long lines unit is received.

```cpp
virtual void OnLongLinesUnitReceived(const char* targetROIDefName, 
                                        const char* taskName, 
                                        const ddn::intermediate_results::CLongLinesUnit *pResult)
```

**Parameters**

`[in] targetROIDefName` The name of the target ROI definition.

`[in] taskName` The name of the task that produced the result.

`[in] pResult` A pointer to the long lines unit.

### OnCornersUnitReceived

Called when a corners unit is received.

```cpp
virtual void OnCornersUnitReceived(const char* targetROIDefName, 
                                    const char* taskName, 
                                    const ddn::intermediate_results::CCornersUnit *pResult)
```

**Parameters**

`[in] targetROIDefName` The name of the target ROI definition.

`[in] taskName` The name of the task that produced the result.

`[in] pResult` A pointer to the corners unit.

### OnCandidateQuadEdgesUnitReceived

Called when a candidate quad edges unit is received.

```cpp
virtual void OnCandidateQuadEdgesUnitReceived(const char* targetROIDefName, 
                                                const char* taskName, 
                                                const ddn::intermediate_results::CCandidateQuadEdgesUnit *pResult)
```

**Parameters**

`[in] targetROIDefName` The name of the target ROI definition.

`[in] taskName` The name of the task that produced the result.

`[in] pResult` A pointer to the candidate quad edges unit.

### OnCandidateBarcodeZonesUnitReceived

Called when a candidate barcode zones unit is received.

```cpp
virtual void OnCandidateBarcodeZonesUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    const dbr::intermediate_results::CCandidateBarcodeZonesUnit *pResult)
```

**Parameters**

`[in] targetROIDefName` The name of the target ROI definition.

`[in] taskName` The name of the task that produced the result.

`[in] pResult` A pointer to the candidate barcode zones unit.

### OnScaledUpBarcodeImageUnitReceived

Called when a scaled up barcode image unit is received.

```cpp
virtual void OnScaledUpBarcodeImageUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    const dbr::intermediate_results::CScaledUpBarcodeImageUnit *pResult)
```

**Parameters**

`[in] targetROIDefName` The name of the target ROI definition.

`[in] taskName` The name of the task that produced the result.

`[in] pResult` A pointer to the scaled up barcode image unit.

### OnDeformationResistedBarcodeImageUnitReceived

Called when a deformation resisted barcode image unit is received.

```cpp
virtual void OnDeformationResistedBarcodeImageUnitReceived(const char* targetROIDefName, 
                                                            const char* taskName, 
                                                            const dbr::intermediate_results::CDeformationResistedBarcodeImageUnit *pResult)
```

**Parameters**

`[in] targetROIDefName` The name of the target ROI definition.

`[in] taskName` The name of the task that produced the result.

`[in] pResult` A pointer to the deformation resisted barcode image unit.

### OnComplementedBarcodeImageUnitReceived

Called when a complemented barcode image unit is received.

```cpp
virtual void OnComplementedBarcodeImageUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    const dbr::intermediate_results::CComplementedBarcodeImageUnit *pResult)
```

**Parameters**

`[in] targetROIDefName` The name of the target ROI definition.

`[in] taskName` The name of the task that produced the result.

`[in] pResult` A pointer to the complemented barcode image unit.
