---
layout: default-layout
title: Utility Module Release Notes - Dynamsoft Capture Vision CPP Edition
description: The release notes of DynamsoftUtility module - Dynamsoft Capture Vision CPP Edition.
keywords: release notes, utility, CPP
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftUtility Module

## 1.2.20 (04/07/2024)

### New

- Added internal logics to output errors when failing to load PDF library.

## 1.2.10 (03/01/2024)

### Improved

- Security update for `DynamsoftUtility` library.

## 1.2.0 (01/16/2024)

### New

- Add C interfaces and implementations, which are only used to encapsulate upper-level languages such as c# and python, etc.

### Break Changes

- Change the compiler option of the runtime library of Windows DLLs from MD to MT.

## 1.0.20 (10/26/2023)

### New

- Added a new method `setPages` to the class `DirectoryFetcher` and class `FileFetcher`.
- The class `DirectoryFetcher` and `FileFetcher` will be able to return error codes via `ImageSourceErrorListener`
- Updated the error codes of the method `saveToFile` of the class `ImageManager`.

### Changed

- Changed the upper limit to the `DuplicateForgetTime`, which is 3 minutes.

## 1.0.10 (08/08/2023)

### New

- Added `CRIT_NORMALIZED_IMAGE` to the available result types of result cross-verification.

### Break Changes

- Renamed the following methods of class `CMultiFrameResultCrossFilter`:
  - from `EnableResultVerification` to `EnableResultCrossVerification`.
  - from `isResultVerificationEnable` to `isResultCrossVerificationEnabled`.
  - from `EnableDuplicateFilter` to `EnableResultDeduplication`.
  - from `isDuplicateFilterEnabled` to `isResultDeduplicationEnabled`.

## 1.0.0 (07/04/2023)

The first version of `DynamsoftUtility` CPP edition.
