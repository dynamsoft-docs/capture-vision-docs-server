---
layout: default-layout
title: DLR Module Release Notes - Dynamsoft Capture Vision CPP Edition
description: The release notes of DynamsoftLabelRecognizer module - Dynamsoft Capture Vision CPP Edition.
keywords: release notes, label recognizer, CPP, DLR
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftLabelRecognizer Module

## 3.2.20 (04/07/2024)

### Improved

- Improved the speed of TextLineGroup detection by optimizing internal logic.

### New

- Added new [`LabelRecognizerTaskSettings`]({{ site.dcv_parameters_reference }}label-recognizer-task-settings/index.html) parameters.
  - Added [`ConfusableCharactersPath`]({{ site.dcv_parameters_reference }}label-recognizer-task-settings/confusable-characters-path.html) to define the path of the resource files that store the confusable characters' information.
  - Added [`ClusterSamplesCountThreshold`]({{ site.dcv_parameters_reference }}label-recognizer-task-settings/cluster-samples-count-threshold.html) to specify the lowest required sample count for clustering.
- Added new [`TextLineSpecification`]({{ site.dcv_parameters_reference }}text-line-specification/index.html) parameters.
  - Added [`ConfusableCharactersCorrection`]({{ site.dcv_parameters_reference }}text-line-specification/confusable-characters-correction.html) to define which confusable characters you are going to distinguish. You can also specify the font type of the characters.
  - Added [`ExpectedGroupCount`]({{ site.dcv_parameters_reference }}text-line-specification/expected-groups-count.html) to define the count of TextLineGroups that might exist on the image.
- Added new classes for the character buffer feature:
  - [`CBufferedCharacterItemSet`]({{ site.dlr_cpp_api }}buffered-character-item-set.html): The class that stores a collection of buffered character items and cluster information.
  - [`CBufferedCharacterItem`]({{ site.dlr_cpp_api }}buffered-character-item.html): The class that stores a basic item of the buffered characters with its image and features information.
  - [`CCharacterCluster`]({{ site.dlr_cpp_api }}character-cluster.html): The class that stores a character cluster generated from the collected buffered character items.
- Added method [`GetSpecificationName`]({{ site.dlr_cpp_api }}text-line-result-item.html) to the `CTextLineResultItem` class to get the name of the `TextLineSpecification`object that generated this `CTextLineResultItem`.
- Added method [`GetSpecificationName`]({{ site.dlr_cpp_api }}recognized-text-line-element.html) to the `CRecognizedTextLineElement` class to get the name of the `TextLineSpecification`object that generated this `CRecognizedTextLineElement`.

## 3.2.10 (03/01/2024)

### Improved

- Security update for `DynamsoftLabelRecognizer` library.
- Supported the filter configuration of the characters that are not recognized by the Deep Neural Network via the `Filter.txt` file.

### Fixed

- Fixed a bug where multiple results were output from the same text area.

## 3.2.0 (01/16/2024)

### New

- Added new methods to the `CLocalizedTextLinesUnit` class to add, set or remove the localized text line elements.
- Added new methods to the `CRecognizedTextLinesUnit` class to add, set or remove the recognized text line elements.
- Added the following methods to the `CRecognizedTextLineElement` class
  - A new constructor (the old one is removed)
  - `SetText`
- Added a new constructor to the `CTextLineResultItem` class to replace the previous one.
- Added the following methods to the `CrecognizedTextLinesResult` class.
  - `operator[]`
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

## 3.0.30 (02/01/2024)

### New

- Added internal logic to obtain resources based on the specified template.

## 3.0.20 (10/26/2023)

### New

- Added the support of the following preset templates:
  - PT_RECOGNIZE_NUMBERS
  - PT_RECOGNIZE_LETTERS
  - PT_RECOGNIZE_NUMBERS_AND_LETTERS
  - PT_RECOGNIZE_NUMBERS_AND_UPPERCASE_LETTERS
  - PT_RECOGNIZE_UPPERCASE_LETTERS
- Added a new parameter scaleDownThreshold to the struct SimplifiedLabelRecognizerSettings.

### Fixed

- Small fixes and tweaks.

## 3.0.10 (08/08/2024)

- Renamed the method `GetSourceImageHashId` of `CRecognizedTextLinesResult` class to `GetOriginalImageHashId`.
- Renamed the method `GetSourceImageTag` of `CRecognizedTextLinesResult` class to `GetOriginalImageTag`.
- Renamed the method `GetCount` of `CRecognizedTextLinesResult` class to `GetItemsCount`.

## 3.0.0 (07/04/2023)

The first version of `DynamsoftLabelRecognizer (DLR)` CPP edition that integrate with `DynamsoftCaptureVision (DCV)` architecture.
