---
layout: default-layout
title: DIP Module Release Notes - Dynamsoft Capture Vision CPP Edition
description: The release notes of DynamsoftImageProcessing module - Dynamsoft Capture Vision CPP Edition.
keywords: release notes, image processing, CPP, DIP
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftImageProcessing Module

## 2.2.30 (05/13/2024)

- Fixed a bug where users would not receive proper error messages when attempting to configure `SimplifiedLabelRecognizerSettings` with an incorrect `CharacterModel`.

## 2.2.20 (04/07/2024)

### New

- Added internal logics to output errors when failing to load PDF library.

## 2.2.10 (03/01/2024)

### Improved

- Security update for `DynamsoftImageProcessing` library.
- Improve security vulnerabilities.

## 2.2.0 (01/16/2024)

### New

- Added a new method `CreatePredetectedRegionElement` to the `CImageProcessingModule` class to create the predetected region element.
- Add C interfaces and implementations, which are only used to encapsulate upper-level languages such as c# and python, etc.

### Break Changes

- The `DeepNeuralNetwork` module is separated from the `DynamsoftImageProcessing` module.
- Change the compiler option of the runtime library of Windows DLLs from MD to MT.

## 2.0.30 (02/01/2024)

### New

- Added internal changes to read code parser task settings parameters.

## 2.0.20 (10/26/2023)

### Fixed

- Small fixes and tweaks.

## 2.0.10 (08/08/2023)

### Fixed

- Small fixes and tweaks.

## 2.0.0 (07/04/2023)

The first version of `DynamsoftImageProcessing` module CPP edition that integrate with `DynamsoftCaptureVision (DCV)` architecture.
