---
layout: default-layout
title: Capture Vision Router API Reference Index- Dynamsoft Capture Vision C++ Edition API Reference
description: This page is the index of the C++ edition API Reference of the Dynamsoft Capture Vision Router Module.
keywords: capture vision, router, c++, api reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: CVR C++ API Reference Index
permalink: /programming/cplusplus/api-reference/capture-vision-router/index.md
---

# Capture Vision Router C++ API Reference Index

The "Capture Vision Router" module is defined in the namespace `Dynamsoft.CVR` which consists of the main class `CCaptureVisionRouter` and a few auxiliary classes and structs.

## Main Class - `CCaptureVisionRouter`

The CCaptureVisionRouter class is what a user uses to interact with image-processing and semantic-processing products in their applications. It accepts an image source and returns processing results which may contain [Final results]({{architecture}}output.md#final-results) or [Intermediate Results]({{architecture}}output.md#intermediate-results).

Read more about the class [`CCaptureVisionRouter`](capture-vision-router.md).

## Auxiliary Classes

The following are the auxiliary classes:

* [CaptureStateListener](auxiliary-classes/capture-state-listener.md)
* [ImageSourceStateListener](auxiliary-classes/image-source-state-listener.md)

## Structs

At present, there is only one struct in the "Capture Vision Router" module:

* [SimplifiedCaptureVisionSettings](structs/simplified-capture-vision-settings.md)

## Enums

* [EnumImageSourceState]({{enums}}core/image-source-state.md?lang=cpp)
* [EnumCaptureState]({{enums}}core/capture-state.md?lang=cpp)
