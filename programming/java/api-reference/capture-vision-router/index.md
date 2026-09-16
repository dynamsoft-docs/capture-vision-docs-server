---
layout: default-layout
title: Capture Vision Router API Reference - Dynamsoft Capture Vision Java Edition
description: API reference index of the DynamsoftCaptureVisionRouter module in Dynamsoft Capture Vision Java Edition, covering the CaptureVisionRouter class, its auxiliary classes, enums, errors and exceptions.
keywords: capture vision router, cvr, java, api reference
needGenerateH3Content: false
---

# Capture Vision Router API Reference - Java Edition

The `DynamsoftCaptureVisionRouter` module consists of the main class `CaptureVisionRouter` and a few auxiliary classes and enumerations.

## Main Class

- [`CaptureVisionRouter`](capture-vision-router.md): The main class that accepts an image source, runs image-processing and semantic-processing tasks, and returns the captured results.
  - [Constructor](instantiate.md)
  - [Single-File Processing](single-file-processing.md)
  - [Multiple-File Processing](multiple-file-processing.md)
  - [Settings](settings.md)
  - [Intermediate Result](intermediate-result.md)
  - [Buffered Items](buffered-items.md)
  - [Auxiliary Methods](auxiliary-methods.md)

## Auxiliary Classes

- [Auxiliary Classes Index](auxiliary-classes/index.md): Class and listener types used with `CaptureVisionRouter`.

## Enums

- [`CaptureState`](enum-capture-state.md): Possible states of the data capture process.
- [`ImageSourceState`](enum-image-source-state.md): States of the image source adapter.
- [`PresetTemplate`](enum-preset-template.md): Built-in preset templates available for common capture scenarios.

## Errors and Exceptions

- [`CaptureVisionError`](capture-vision-error.md): Error codes specific to the Capture Vision Router module.
- [`CaptureVisionException`](capture-vision-exception.md): Exception class providing error code and message for CVR module errors.
