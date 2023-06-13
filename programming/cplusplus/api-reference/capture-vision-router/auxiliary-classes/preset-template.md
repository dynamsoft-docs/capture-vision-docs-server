---
layout: default-layout
title: class CPresetTemplate - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the C++ edition of the class CPresetTemplate in Dynamsoft Capture Vision Router Module.
keywords: preset template, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: CVR C++ CPresetTemplate Class
permalink: /programming/cplusplus/api-reference/capture-vision-router/auxiliary-classes/preset-template.html
---

# CPresetTemplate

The `CPresetTemplate` class defines all preset template names of Capture Vision SDK.

## Definition

*Namespace:* dynamsoft::cvr

*Assembly:* DynamsoftCaptureVisionRouter.dll

```cpp
class CPresetTemplate 
```

## Attributes Summary

| Attribute                                             | Type                                | Description|
| ----------------------------------------------------- | ----------------------------------- |------------|
| [`PT_DEFAULT`](#pt_default)                           | *const char\**                      | Template name: "default". It supports barcode decoding, label recognizing and document normalizing. |
| [`PT_READ_BARCODES`](#pt_read_barcodes)               | *const char\**                      | Template name: "read-barcodes". It only supports barcode decoding. |
| [`PT_RECOGNIZE_TEXT_LINES`](#pt_recognize_text_lines) | *const char\**                      | Template name: "recognize-textLines". It only supports label recognition. |
| [`PT_DETECT_DOCUMENT_BOUNDARIES`](#pt_detect_document_boundaries)| *const char\**           | Template name: "detect-document-boundaries". It only supports detecting document boundaries. |
| [`PT_DETECT_AND_NORMALIZE_DOCUMENT`](#pt_detect_and_normalize_document)| *const char\**     | Template name: "detect-and-normalize-document". It supports detecting document boundaries and normalizing documents. |
| [`PT_NORMALIZE_DOCUMENT`](#pt_normalize_document)                 | *const char\**          | Template name: "normalize-document". It only supports normalizing documents. |
