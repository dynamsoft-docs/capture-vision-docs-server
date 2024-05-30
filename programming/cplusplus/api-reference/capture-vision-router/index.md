---
layout: default-layout
title: Capture Vision Router API Reference Index- Dynamsoft Capture Vision C++ Edition API Reference
description: This page is the index of the C++ edition API Reference of the Dynamsoft Capture Vision Router Module.
keywords: capture vision, router, c++, api reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: CVR C++ API Reference Index
---

# Capture Vision Router C++ API Reference Index

The "Capture Vision Router" module is defined in the namespace `dynamsoft::cvr` which consists of the main class `CCaptureVisionRouter` and a few auxiliary classes and structs.

## Main Class - `CCaptureVisionRouter`

The CCaptureVisionRouter class is what a user uses to interact with image-processing and semantic-processing products in their applications. It accepts an image source and returns processing results which may contain [Final results]({{site.dcv_architecture}}output.md#final-results) or [Intermediate Results]({{site.dcv_architecture}}output.md#intermediate-results).

Read more about the class [`CCaptureVisionRouter`](capture-vision-router.md).

## Auxiliary Classes

The following are the auxiliary classes:

* [CCaptureStateListener](auxiliary-classes/capture-state-listener.md)
* [CImageSourceStateListener](auxiliary-classes/image-source-state-listener.md)
* [CCapturedResultReceiver](auxiliary-classes/captured-result-receiver.md)
* [CIntermediateResultReceiver](auxiliary-classes/intermediate-result-receiver.md)
* [CIntermediateResultManager](auxiliary-classes/intermediate-result-manager.md)
* [CCapturedResult](auxiliary-classes/captured-result.md)
* [CBufferedItemsManager](auxiliary-classes/buffered-items-manager.md)

## Structs

At present, there is only one struct in the "Capture Vision Router" module:

* [SimplifiedCaptureVisionSettings](structs/simplified-capture-vision-settings.md)

## Enums

* [ImageSourceState]({{site.dcv_enumerations}}capture-vision-router/image-source-state.md?lang=cpp)
* [CaptureState]({{site.dcv_enumerations}}capture-vision-router/capture-state.md?lang=cpp)
