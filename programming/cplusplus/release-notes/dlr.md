---
layout: default-layout
title: DLR Module Release Notes - Dynamsoft Capture Vision CPP Edition
description: The release notes of DynamsoftLabelRecognizer module - Dynamsoft Capture Vision CPP Edition.
keywords: release notes, label recognizer, CPP, DLR
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftLabelRecognizer Module

## 3.2.0 (01/16/2024)

### New

- Added new methods to the `CLocalizedTextLinesUnit` class to add, set or remove the localized text line elements.
- Added new methods to the `CRecognizedTextLinesUnit` class to add, set or remove the recognized text line elements.
- Added the following methods to the `CRecognizedTextLineElement` class
  - A new constructor (the old one is removed)
  - `SetText`
- Added a new constructor to the `CTextLineResultItem` class to replace the previous one.
- Added the following methods to the `CrecognizedTextLinesResult` class.
  - A new constructor
  - `Retain`
  - `Release`
- Added the following methods to the `CLabelRecognizerModule` class to create the corresponding elements.
  - `CreateRecognizedTextLineElement`
  - `CreateLocalizedTextLineElement`
- Add C interfaces and implementations, which are only used to encapsulate upper-level languages such as c# and python, etc.

### Break Changes

- The destructor functions of the following classes are changed to protected:
  - `CLocalizedTextLineElement`
  - `CLocalizedTextLinesUnit`
  - `CRecognizedTextLineElement`
  - `CRecognizedTextLinesUnit`
  - `CRecognizedTextLinesResult`
- Change the compiler option of the runtime library of Windows DLLs from MD to MT.

## 3.0.10 (08/08/2024)

- Renamed the method `GetSourceImageHashId` of `CRecognizedTextLinesResult` class to `GetOriginalImageHashId`.
- Renamed the method `GetSourceImageTag` of `CRecognizedTextLinesResult` class to `GetOriginalImageTag`.
- Renamed the method `GetCount` of `CRecognizedTextLinesResult` class to `GetItemsCount`.

## 3.0.0 (07/04/2023)

The first version of `DynamsoftLabelRecognizer (DLR)` CPP edition that integrate with `DynamsoftCaptureVision (DCV)` architecture.
