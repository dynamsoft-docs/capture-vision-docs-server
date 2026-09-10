---
layout: default-layout
title: Capture Vision Router API Reference - Dynamsoft Capture Vision C++ Edition
description: API reference index of the DynamsoftCaptureVisionRouter module in Dynamsoft Capture Vision C++ Edition, covering the CCaptureVisionRouter class, its auxiliary classes, structs and enums.
keywords: capture vision router, cvr, c++, api reference
needGenerateH3Content: false
---

# Capture Vision Router API Reference - C++ Edition

The `DynamsoftCaptureVisionRouter` module consists of the main class `CCaptureVisionRouter` and a few auxiliary classes, structs and enumerations.

## Main Class

- [`CCaptureVisionRouter`](capture-vision-router.md): The main class that accepts an image source, runs image-processing and semantic-processing tasks, and returns the captured results.
  - [Constructor and Destructor](instantiate.md)
  - [Single-File Processing](single-file-processing.md)
  - [Multiple-File Processing](multiple-file-processing.md)
  - [Settings](settings.md)
  - [Intermediate Result](intermediate-result.md)
  - [Buffered Items](buffered-items.md)
  - [Auxiliary Methods](auxiliary-methods.md)

## Auxiliary Classes

- [Auxiliary Classes Index](auxiliary-classes/index.md): Listener, receiver, filter, manager and result classes used with `CCaptureVisionRouter`.

## Structs

- [Structs Index](structs/index.md): Data structures used by the module.

## Enums

- [`CaptureState`](enum-capture-state.md): Possible states of the data capture process.
- [`ImageSourceState`](enum-image-source-state.md): States of the image source adapter.
