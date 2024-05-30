---
layout: default-layout
title: PresetTemplate Class - Dynamsoft Capture Vision Module .NET Edition API Reference
description: Definition of PresetTemplate class in Dynamsoft Capture Vision Module .NET Edition.
keywords: preset template, .NET
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# PresetTemplate

The `PresetTemplate` class defines all preset template names of Capture Vision SDK.

## Definition

*Namespace:* Dynamsoft.CVR

*Assembly:* Dynamsoft.CaptureVisionRouter.dll

```csharp
public class PresetTemplate 
```

## Attributes

| Attribute | Type | Description |
| --------- | ---- |------------ |
| `PT_DEFAULT` | *string* | Template name: "Default". It supports barcode decoding, label recognizing and document normalizing. |
| `PT_READ_BARCODES` | *string* | Template name: "ReadBarcodes_Default". It only supports barcode decoding. |
| `PT_RECOGNIZE_TEXT_LINES` | *string* | Template name: "RecognizeTextLines_Default". It only supports label recognition. |
| `PT_DETECT_DOCUMENT_BOUNDARIES` | *string* | Template name: "DetectDocumentBoundaries_Default". It only supports detecting document boundaries. |
| `PT_DETECT_AND_NORMALIZE_DOCUMENT` | *string* | Template name: "DetectAndNormalizeDocument_Default". It supports detecting document boundaries and normalizing documents. |
| `PT_NORMALIZE_DOCUMENT` | *string* | Template name: "NormalizeDocument_Default". It only supports normalizing documents. |
| `PT_READ_BARCODES_SPEED_FIRST` | *string* | Template name: "ReadBarcodes_SpeedFirst". Represents a barcode reading mode where speed is prioritized. |
| `PT_READ_BARCODES_READ_RATE_FIRST` | *string* | Template name: "ReadBarcodes_ReadRateFirst". Represents a barcode reading mode where barcode read rate is prioritized. |
| `PT_READ_SINGLE_BARCODE` | *string* | Template name: "ReadSingleBarcode". Represents a barcode reading mode for single barcode code detection. |
| `PT_RECOGNIZE_NUMBERS` | *string* | Template name: "RecognizeNumbers". Represents a text recognition mode focused on recognizing numbers. |
| `PT_RECOGNIZE_LETTERS` | *string* | Template name: "RecognizeLetters". Represents a text recognition mode focused on recognizing alphabetic characters (letters). |
| `PT_RECOGNIZE_NUMBERS_AND_LETTERS` | *string* | Template name: "RecognizeNumbersAndLetters". Represents a text recognition mode that combines numbers and alphabetic characters (letters) recognition. |
| `PT_RECOGNIZE_NUMBERS_AND_UPPERCASE_LETTERS` | *string* | Template name: "RecognizeNumbersAndUppercaseLetters". Represents a text recognition mode that combines numbers and uppercase letters recognition. |
| `PT_RECOGNIZE_UPPERCASE_LETTERS` | *string* | Template name: "RecognizeUppercaseLetters". Represents a text recognition mode focused on recognizing uppercase letters. |
