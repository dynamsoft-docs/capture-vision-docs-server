---
layout: default-layout
title: Capture Vision Router Class- Dynamsoft Capture Vision C++ Edition API Reference
description: This page is about the Capture Vision Router Class of the C++ edition of the Dynamsoft Capture Vision Router Module.
keywords: capture vision router, router, c++, api reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: CVR C++ CCaptureVisionRouter Class
permalink: /programming/cplusplus/api-reference/capture-vision-router/capture-vision-router.html
---

# CCaptureVisionRouter

The CCaptureVisionRouter class is what a user uses to interact with image-processing and semantic-processing products in their applications. It accepts an image source and returns processing results which may contain [Final results]({{site.architecture}}output.html#final-results) or [Intermediate Results]({{site.architecture}}output.html#intermediate-results).

The APIs for this class include:

## Constructor and Destructor

| Method                                                           | Description                                           |
| ---------------------------------------------------------------- | ----------------------------------------------------- |
| [`CCaptureVisionRouter`](instantiate.md#ccapturevisionrouter)    | Default constructor of `CCaptureVisionRouter` object. |
| [`~CCaptureVisionRouter`](instantiate.md#ccapturevisionrouter-1) | Destructor of `CCaptureVisionRouter` object.          |

## Single-File Processing

| API Name                                       | Description                                               |
| ---------------------------------------------- | --------------------------------------------------------- |
| [capture()](single-file-processing.md#capture) | Process an image or file to derive important information. |

## Multiple-File Processing

| API Name                                                                                       | Description                                                                  |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| [SetInput()](multiple-file-processing.md#setinput)                                             | Sets an image source to provide images for consecutive process.              |
| [GetInput()](multiple-file-processing.md#getinput)                                             | Get the object of CImageSourceAdapter that act as the input.                 |
| [AddCaptureStateListener()](multiple-file-processing.md#addcapturestatelistener)               | Adds an object that listens to the state changes of the capture process.     |
| [RemoveCaptureStateListener()](multiple-file-processing.md#removecapturestatelistener)         | Removes an object which listens to the state changes of the capture process. |
| [AddImageSourceStateListener()](multiple-file-processing.md#addimagesourcestatelistener)       | Adds an object that listens to state changes of the image source.            |
| [RemoveImageSourceStateListener()](multiple-file-processing.md#removeimagesourcestatelistener) | Removes an object which listens to state changes of the image source.        |
| [AddResultReceiver()](multiple-file-processing.md#addresultreceiver)                           | Adds an object as the receiver of captured results.                          |
| [RemoveResultReceiver()](multiple-file-processing.md#removeresultreceiver)                     | Removes an object which was added as a receiver of captured results.         |
| [StartCapturing()](multiple-file-processing.md#startcapturing)                                 | Starts to process images consecutively.                                      |
| [StopCapturing()](multiple-file-processing.md#stopcapturing)                                   | Stops the consecutive process.                                               |

## Settings

| API Name                                                     | Description                                                                                  |
| ------------------------------------------------------------ | -------------------------------------------------------------------------------------------- |
| [`InitSettings`](settings.md#initsettings)                   | Loads and initializes a template from a string.                                              |
| [`InitSettingsFromFile`](settings.md#initsettingsfromfile)   | Loads and initializes a template from a file.                                                |
| [`OutputSettings`](settings.md#outputsettings)               | Exports a specific `CaptureVisionTemplate` to a string.                                      |
| [`OutputSettingsToFile`](settings.md#outputsettingstofile)   | Exports a specific `CaptureVisionTemplate` to a file.                                        |
| [`GetSimplifiedSettings`](settings.md#getsimplifiedsettings) | Retrieves a `SimplifiedCaptureVisionSettings` object for a specific `CaptureVisionTemplate`. |
| [`UpdateSettings`](settings.md#updatesettings)               | Updates a `CaptureVisionTemplate` with `SimplifiedCaptureVisionSettings` object.             |
| [`ResetSettings`](settings.md#resetsettings)                 | Resets all templates to factory settings.                                                    |

## Intermediate Result

The following method returns an `CIntermediateResultManager` object which allows the application to tap into the algorithmic process.

| API Name                                                                            | Description                                     |
| ----------------------------------------------------------------------------------- | ----------------------------------------------- |
| [GetIntermediateResultManager](intermediate-result.md#getintermediateresultmanager) | Returns an `CIntermediateResultManager` object. |

## Auxiliary

| API Name                                      | Description                                               |
| --------------------------------------------- | --------------------------------------------------------- |
| [GetVersion](auxiliary-methods.md#getversion) | Returns the version of the `CCaptureVisionRouter` object. |
| [FreeString](auxiliary-methods.md#freestring) | Frees the memory allocated for a string.                  |
