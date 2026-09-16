---
layout: default-layout
title: Capture Vision Router Auxiliary Classes - Dynamsoft Capture Vision C++ Edition API Reference
description: API reference index of the auxiliary classes in the DynamsoftCaptureVisionRouter module, including listeners, receivers, filters, managers and result classes.
keywords: capture vision router, auxiliary classes, c++, api reference
needGenerateH3Content: false
---

# Auxiliary Classes

The following auxiliary classes are used together with `CCaptureVisionRouter`:

- [`CBufferedItemsManager`](buffered-items-manager.md): Manages the buffer of recognized character items for cross-frame verification.
- [`CCaptureStateListener`](capture-state-listener.md): Callback interface notified when the capture state changes.
- [`CCapturedResult`](captured-result.md): Represents the collection of all result items from a single image capture.
- [`CCapturedResultArray`](captured-result-array.md): Represents an array of `CCapturedResult` objects returned from multi-page or batch processing.
- [`CCapturedResultFilter`](captured-result-filter.md): Defines rules to filter captured results.
- [`CCapturedResultReceiver`](captured-result-receiver.md): Callback interface for receiving captured results.
- [`CCaptureVisionRouterModule`](capture-vision-router-module.md): Provides module-level utilities such as version retrieval.
- [`CImageSourceStateListener`](image-source-state-listener.md): Callback interface notified when the image source state changes.
- [`CIntermediateResultManager`](intermediate-result-manager.md): Manages registration and retrieval of intermediate processing results.
- [`CIntermediateResultReceiver`](intermediate-result-receiver.md): Callback interface for receiving intermediate results during image processing.
- [`CPresetTemplate`](preset-template.md): Provides string constants for built-in preset template names.
