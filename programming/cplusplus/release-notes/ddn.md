---
layout: default-layout
title: DDN Module Release Notes - Dynamsoft Capture Vision CPP Edition
description: The release notes of DynamsoftDocumentNormalizer module - Dynamsoft Capture Vision CPP Edition.
keywords: release notes, document normalizer, CPP, DDN
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftDocumentNormalizer Module

## 2.2.0 (01/16/2024)

### New

- Added new methods to the `CLongLinesUnit` class to add, set or remove the line segments of the unit.
- Added new methods to the `CCornersUnit` class to add, set or remove the corners of the unit.
- Added new methods to the `CCandidateQuadEdgesUnit` class to add, set or remove the candidate quad edges of the unit.
- Added new methods to the `CDetectedQuadsUnit` class to add, set or remove the detected quad elements of the unit.
- Added new methods to the `CNormalizedImagesUnit` class to set or remove the normalized image element of the unit.
- Added the following methods to the `CNormalizedImagesResult` class.
  - A new constructor
  - `Retain`
  - `Release`
- Added the following methods to the `CDetectedQuadsResult` class.
  - A new constructor
  - `Retain`
  - `Release`
- Added `SimplifiedDocumentNormalizerSettings` struct to configure basic settings of document processing.
- Added the following methods to the `CDocumentNormalizerModule` class to create the corresponding elements:
  - `CreateNormalizedImageElement`
  - `CreateDetectedQuadElement`
- Added a new enumeration `ImageColourMode` to specify the colour mode of the normalized image.
- Add C interfaces and implementations, which are only used to encapsulate upper-level languages such as c# and python, etc.

### Break Changes

- The destructor functions of the following classes are changed to protected:
  - `CCandidateQuadEdgesUnit`
  - `CCornersUnit`
  - `CDetectedQuadElement`
  - `CDetectedQuadsUnit`
  - `CLongLinesUnit`
  - `CNormalizedImageElement`
  - `CNormalizedImageUnit`
  - `CNormalizedImagesResult`
  - `CDetectedQuadsResult`
- Change the compiler option of the runtime library of Windows DLLs from MD to MT.

## 2.0.20 (10/26/2023)

### Changed

- Updated the SDK to compatible with `DynamsoftCaptureVisionRouter` v2.0.21.
- Updated the dependency rules of Dynamsoft SDK modules. Removed transitive dependencies.

### Fixed

- Small fixes and tweaks.

## 2.0.10 (08/08/2023)

### New

- Added `CRIT_NORMALIZED_IMAGE` to the available result types of result cross-verification.

### Break Changes

- Changed the parameters and the return value of the method `GetLongLine` of `CLongLinesUnit` class. The method will require an index value as the parameter and return a `CLineSegment` object as the return value.
- Renamed method `GetSourceImageHashId` to `GetOriginalImageHashId`. This change applies to the following classes:
  - `CNormalizedImagesResult`
  - `CDetectedQuadsResult`
- Renamed method `GetSourceImageTag` to `GetOriginalImageTag`. This change applies to the following classes:
  - `CNormalizedImagesResult`
  - `CDetectedQuadsResult`
- Renamed methods `GetCount` to `GetItemsCount`. This change applies to the following classes:
  - `CNormalizedImagesResult`
  - `CDetectedQuadsResult`
- Renamed parameter `CornerAngleRangeArray` to `CornerAngleRange`. The range of the sub parameter MinValue is restricted to [0,90] and the range of `MaxValue` is restricted to [90,180].

## 2.0.0 (07/04/2023)

The first version of `DynamsoftDocumentNormalizer (DDN)` CPP edition that integrate with `DynamsoftCaptureVision (DCV)` architecture.
