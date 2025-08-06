---
layout: default-layout
title: PresetTemplate - Dynamsoft Vision Router Java Enumerations
description: The enumeration PresetTemplate of Dynamsoft Vision Router describes the preset template.
keywords: Capture state
---

# Enumeration PresetTemplate

`PresetTemplate` describes the preset template names.

```java
@interface EnumPresetTemplate {
   // Template name: "Default". It supports barcode decoding, label recognizing and document normalizing.
   String PT_DEFAULT = "Default";
   // Template name: "ReadBarcodes_Default". It only supports barcode decoding.
   String PT_READ_BARCODES = "ReadBarcodes_Default";
   // Template name: "RecognizeTextLines_Default". It only supports label recognition.
   String PT_RECOGNIZE_TEXT_LINES = "RecognizeTextLines_Default";
   // Template name: "DetectDocumentBoundaries_Default". It only supports detecting document boundaries.
   String PT_DETECT_DOCUMENT_BOUNDARIES = "DetectDocumentBoundaries_Default";
   // Template name: "DetectAndNormalizeDocument_Default". It supports detecting document boundaries and normalizing documents.
   String PT_DETECT_AND_NORMALIZE_DOCUMENT = "DetectAndNormalizeDocument_Default";
   // Template name: "NormalizeDocument_Default". It only supports normalizing documents.
   String PT_NORMALIZE_DOCUMENT = "NormalizeDocument_Default";
   // Template name: "ReadBarcodes_SpeedFirst". Represents a barcode reading mode where speed is prioritized.
   String PT_READ_BARCODES_SPEED_FIRST = "ReadBarcodes_SpeedFirst";
   // Template name: "ReadBarcodes_ReadRateFirst". Represents a barcode reading mode where barcode read rate is prioritized.
   String PT_READ_BARCODES_READ_RATE_FIRST = "ReadBarcodes_ReadRateFirst";
   // Template name: "ReadSingleBarcode". Represents a barcode reading mode for single barcode code detection.
   String PT_READ_SINGLE_BARCODE = "ReadSingleBarcode";
   // Template name: "RecognizeNumbers". Represents a text recognition mode focused on recognizing numbers.
   String PT_RECOGNIZE_NUMBERS = "RecognizeNumbers";
   // Template name: "RecognizeLetters". Represents a text recognition mode focused on recognizing alphabetic characters (letters).
   String PT_RECOGNIZE_LETTERS = "RecognizeLetters";
   // Template name: "RecognizeNumbersAndLetters". Represents a text recognition mode that combines numbers and alphabetic characters (letters) recognition.
   String PT_RECOGNIZE_NUMBERS_AND_LETTERS = "RecognizeNumbersAndLetters";
   // Template name: "RecognizeNumbersAndUppercaseLetters". Represents a text recognition mode that combines numbers and uppercase letters recognition.
   String PT_RECOGNIZE_NUMBERS_AND_UPPERCASE_LETTERS = "RecognizeNumbersAndUppercaseLetters";
   // Template name: "RecognizeUppercaseLetters". Represents a text recognition mode focused on recognizing uppercase letters.
   String PT_RECOGNIZE_UPPERCASE_LETTERS = "RecognizeUppercaseLetters";
}
```