---
layout: default-layout
title: DLR Module Release Notes - Dynamsoft Capture Vision CPP Edition
description: The release notes of DynamsoftLabelRecognizer module - Dynamsoft Capture Vision CPP Edition.
keywords: release notes, label recognizer, CPP, DLR
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftLabelRecognizer Module

## 3.4.10 (07/23/2024)

<!-- Added internal logic for usage count. -->
### New

- Added a new parameter CharSet to the [`CharacterModel`]({{ site.dcv_parameters }}character-model/) object to include or exclude characters for recognition.
- Added a new algorithm stage `IRUT_RAW_TEXT_LINES`. Corresponding APIs are added to obtain the intermediate result of this stage.
  - Class [`CRawTextLinesUnit`]({{ site.dlr_cpp_api }}raw-text-lines-unit.html)
  - Class [`CRawTextLine`]({{ site.dlr_cpp_api }}raw-text-line.html)
  - Enumeration [`RawTextLineStatus`]({{ site.dlr_cpp_api }}raw-text-line-status.html)
- Added the following intermediate result altering functions to the class [`CRecognizedTextLinesUnit`]({{ site.dlr_cpp_api }}recognized-text-lines-unit.html).
  - Added function [`RemoveRecognizedTextLine`]({{ site.dlr_cpp_api }}recognized-text-lines-unit.html#removerecognizedtextLine)
  - Added function [`AddRecognizedTextLine`]({{ site.dlr_cpp_api }}recognized-text-lines-unit.html#addrecognizedtextline)
  - Added function [`SetRecognizedTextLine(index,element,matrixToOriginalImage)`]({{ site.dlr_cpp_api }}recognized-text-lines-unit.html#setrecognizedtextlineindexelementmatrixtooriginalimage)
- Added a new function [`CreateRawTextLine`]({{ site.dlr_cpp_api }}raw-text-lines-unit.html#createRawTextLine) to the class [`CLabelRecognizerModule`]({{ site.dlr_cpp_api }}label-recognizer-module.html).
- Added a new function [`GetRawText`]({{ site.dlr_cpp_api }}text-line-result-item.html#getrawtext) to the class [`CRecognizedTextLineELement`]({{ site.dlr_cpp_api }}recognized-text-line-element.html).
- Added a new function [`GetRawText`]({{ site.dlr_cpp_api }}text-line-result-item.html#getrawtext) to the class [`CTextLineResultItem`]({{ site.dlr_cpp_api }}text-line-result-item.html).
- Added a new function [`AddItem`]({{ site.dlr_cpp_api }}recognized-text-lines-result.html#additem) to the class [`CRecognizedTextLinesResult`]({{ site.dlr_cpp_api }}recognized-text-lines-result.html).
- Added a new function [`SetLocation`]({{ site.dlr_cpp_api }}text-line-result-item.html#setlocation) to the class [`CTextLineResultItem`]({{ site.dlr_cpp_api }}text-line-result-item.html).

### Deprecated

- Deprecated function [`SetRecognizedTextLine(element,matrixToOriginalImage)`]({{ site.dlr_cpp_api }}recognized-text-lines-unit.html#setrecognizedtextlineelementmatrixtooriginalimage) of the class [`CRecognizedTextLinesUnit`]({{ site.dlr_cpp_api }}recognized-text-lines-unit.html).

## 3.2.30 (05/13/2024)

### Fixed

- Fixed a bug where users would not receive proper error messages when attempting to configure `SimplifiedLabelRecognizerSettings` with an incorrect `CharacterModel`.
- Fixed a bug where the characters might not be correctly excluded when they are configured in the filter file.

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
