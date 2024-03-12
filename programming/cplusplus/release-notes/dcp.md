---
layout: default-layout
title: DCP Module Release Notes - Dynamsoft Capture Vision CPP Edition
description: The release notes of DynamsoftCodeParser module - Dynamsoft Capture Vision CPP Edition.
keywords: release notes, code parser, CPP, DCP
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftCodeParser Module

## 2.2.10 (03/01/2024)

### Improved

- Security update for `DynamsoftCodeParser` library.

## 2.2.0 (01/16/2024)

### New

- Added the following methods to the `CParsedResult` class:
  - `operator[]`
  - `Retain`
  - `Release`
- Add C interfaces and implementations, which are only used to encapsulate upper-level languages such as c# and python, etc.

### Break Changes

- The destructor functions of the following classes are changed to protected:
  - `CParsedResultItem`
  - `CParsedResult`
- Removed an internal logic that grouping the text line recognition result of the MRZ. The logic is replaced by the text line group definition of the parameter system.
- Change the compiler option of the runtime library of Windows DLLs from MD to MT.

## 2.0.10 (08/08/2023)

### Fixed

- Small fixes and tweaks.

## 2.0.0 (7/04/2023)

### Highlights

- `DynamsoftCodeParser` SDK has been revamped to integrate with `DynamsoftCaptureVision (DCV)` architecture, which is newly established to aggregate the features of functional products powered by Dynamsoft. The features are designed to be pluggable, customizable and interactable. In addition, the functional products share the computation so that their processing speed is much higher than working individually.
- Added C++ Edition. With this new edition, developers can effortlessly integrate code parsing capabilities into their C++ applications.
- Added supports to parse following code types:
  - MRTD_TD1_ID
  - MRTD_TD2_ID
  - MRTD_TD2_VISA
  - MRTD_TD3_PASSPORT
  - MRTD_TD3_VISA
  - VIN
  - AAMVA_DL_ID
  - AAMVA_DL_ID_WITH_MAG_STRIPE
  - AADHAAR
  - SOUTH_AFRICA_DL
