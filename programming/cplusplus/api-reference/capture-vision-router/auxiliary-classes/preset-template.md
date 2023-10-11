---
layout: default-layout
title: class CPresetTemplate - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the C++ edition of the class CPresetTemplate in Dynamsoft Capture Vision Router Module.
keywords: preset template, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: CVR C++ CPresetTemplate Class
---

# CPresetTemplate

The `CPresetTemplate` class defines all preset template names of Capture Vision SDK.

## Definition

*Namespace:* dynamsoft::cvr

*Assembly:* DynamsoftCaptureVisionRouter

```cpp
class CPresetTemplate 
```

## Attributes Summary

| Attribute | Type | Description |
| --------- | ---- |------------ |
| `PT_DEFAULT` | *const char\** | Template name: "Default". It supports barcode decoding, label recognizing and document normalizing. |
| `PT_READ_BARCODES` | *const char\** | Template name: "ReadBarcodes_Default". It only supports barcode decoding. |
| `PT_RECOGNIZE_TEXT_LINES` | *const char\** | Template name: "RecognizeTextLines_Default". It only supports label recognition. |
| `PT_DETECT_DOCUMENT_BOUNDARIES` | *const char\** | Template name: "DetectDocumentBoundaries_Default". It only supports detecting document boundaries. |
| `PT_DETECT_AND_NORMALIZE_DOCUMENT` | *const char\** | Template name: "DetectAndNormalizeDocument_Default". It supports detecting document boundaries and normalizing documents. |
| `PT_NORMALIZE_DOCUMENT` | *const char\** | Template name: "NormalizeDocument_Default". It only supports normalizing documents. |
| `PT_READ_BARCODES_SPEED_FIRST` | *const char\** | Template name: "ReadBarcodes_SpeedFirst". Represents a barcode reading mode where speed is prioritized. |
| `PT_READ_BARCODES_READ_RATE_FIRST` | *const char\** | Template name: "ReadBarcodes_ReadRateFirst". Represents a barcode reading mode where barcode read rate is prioritized. |
| `PT_READ_SINGLE_BARCODE` | *const char\** | Template name: "ReadSingleBarcode". Represents a barcode reading mode for single barcode code detection. |
| `PT_RECOGNIZE_NUMBERS` | *const char\** | Template name: "RecognizeNumbers". Represents a text recognition mode focused on recognizing numbers. |
| `PT_RECOGNIZE_LETTERS` | *const char\** | Template name: "RecognizeLetters". Represents a text recognition mode focused on recognizing alphabetic characters (letters). |
| `PT_RECOGNIZE_NUMBERS_AND_LETTERS` | *const char\** | Template name: "RecognizeNumbersAndLetters". Represents a text recognition mode that combines numbers and alphabetic characters (letters) recognition. |
| `PT_RECOGNIZE_NUMBERS_AND_UPPERCASE_LETTERS` | *const char\** | Template name: "RecognizeNumbersAndUppercaseLetters". Represents a text recognition mode that combines numbers and uppercase letters recognition. |
| `PT_RECOGNIZE_UPPERCASE_LETTERS` | *const char\** | Template name: "RecognizeUppercaseLetters". Represents a text recognition mode focused on recognizing uppercase letters. |
