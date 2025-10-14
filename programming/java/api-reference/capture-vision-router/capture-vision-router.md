---
layout: default-layout
title: CaptureVisionRouter Class- Dynamsoft Capture Vision Router Module Java Edition API Reference
description: This page is about the CaptureVisionRouter Class of Dynamsoft Capture Vision Router Module Java Edition.
keywords: capture vision router, router, java, api reference
---

# CaptureVisionRouter

The `CaptureVisionRouter` class is what a user uses to interact with image-processing and semantic-processing products in their applications. It accepts an image source and returns processing results which may contain [Final results]({{ site.dcvb_architecture }}output.html#final-results?lang=java).

## Definition

*Namespace:* com.dynamsoft.cvr

```java
class CaptureVisionRouter
```

## Constructor Methods

| Method | Description |
| ------ | ----------- |
| [`CaptureVisionRouter`](instantiate.md#capturevisionrouter) | Initializes a new instance of the `CaptureVisionRouter` class. |

## Single-File Processing Methods

| Method                                         | Description                                               |
| ---------------------------------------------- | --------------------------------------------------------- |
| [`capture`](single-file-processing.md#capture) | Processes an image or file to derive important information. |
| [`captureMultiPages`](single-file-processing.md#capturemultipages) | Processes an image or file containing multiple pages to derive important information. |

## Multiple-File Processing Methods

| Method | Description |
| ------- | ---------- |
| [`setInput`](multiple-file-processing.md#setinput)                                             | Sets an image source to provide images for consecutive process.              |
| [`getInput`](multiple-file-processing.md#getinput)                                             | Gets the attached image source adapter object of the capture vision router.  |
| [`addCaptureStateListener`](multiple-file-processing.md#addcapturestatelistener)               | Adds an object that listens to the state changes of the capture process.     |
| [`removeCaptureStateListener`](multiple-file-processing.md#removecapturestatelistener)         | Removes an object which listens to the state changes of the capture process. |
| [`addImageSourceStateListener`](multiple-file-processing.md#addimagesourcestatelistener)       | Adds an object that listens to state changes of the image source.            |
| [`removeImageSourceStateListener`](multiple-file-processing.md#removeimagesourcestatelistener) | Removes an object which listens to state changes of the image source.        |
| [`addResultReceiver`](multiple-file-processing.md#addresultreceiver)                           | Adds an object as the receiver of captured results.                          |
| [`removeResultReceiver`](multiple-file-processing.md#removeresultreceiver)                     | Removes an object which was added as a receiver of captured results.         |
| [`addResultFilter`](multiple-file-processing.md#addresultfilter)                               | Adds an object as the filter of captured results.                            |
| [`removeResultFilter`](multiple-file-processing.md#removeresultfilter)                         | Removes an object which was added as a filter of captured results.           |
| [`startCapturing`](multiple-file-processing.md#startcapturing)                                 | Starts to process images consecutively.                                      |
| [`stopCapturing`](multiple-file-processing.md#stopcapturing)                                   | Stops the consecutive process.                                               |
| [`pauseCapturing`](multiple-file-processing.md#pausecapturing)                                 | Pauses the capture process. The current thread will be blocked until the capture process is resumed. |
| [`resumeCapturing`](multiple-file-processing.md#resumecapturing)                               | Resumes the capture process. The current thread will be unblocked after the capture process is resumed. |

## Setting Methods

| Method                                                       | Description                                                                                  |
| ------------------------------------------------------------ | -------------------------------------------------------------------------------------------- |
| [`initSettings`](settings.md#initsettings)                   | Loads and initializes a template from a string.                                              |
| [`initSettingsFromFile`](settings.md#initsettingsfromfile)   | Loads and initializes a template from a file.                                                |
| [`outputSettings`](settings.md#outputsettings)               | Exports a specific `CaptureVisionTemplate` to a string.                                      |
| [`outputSettingsToFile`](settings.md#outputsettingstofile)   | Exports a specific `CaptureVisionTemplate` to a file.                                        |
| [`getSimplifiedSettings`](settings.md#getsimplifiedsettings) | Retrieves a `SimplifiedCaptureVisionSettings` object for a specific `CaptureVisionTemplate`. |
| [`updateSettings`](settings.md#updatesettings)               | Updates a `CaptureVisionTemplate` with `SimplifiedCaptureVisionSettings` object.             |
| [`resetSettings`](settings.md#resetsettings)                 | Resets all templates to factory settings.                                                    |
| [`getParameterTemplateCount`](settings.md#getparametertemplatecount)  | Retrieves the total number of available parameter templates.                                 |
| [`getParameterTemplateName`](settings.md#getparametertemplatename)    | Retrieves the name of a specific parameter template by its index.                            |
| [`switchCapturingTemplate`](settings.md#switchcapturingtemplate)    | Switches the capturing template during the image processing workflow.                            |

## Buffered Items Methods

| Method                                                       | Description                                                                                  |
| ------------------------------------------------------------ | -------------------------------------------------------------------------------------------- |
| [`getBufferedItemsManager`](buffered-items.md#getbuffereditemsmanager)                   | Gets a `BufferedItemsManager` object.  |

## Intermediate Result

The following method returns an `IntermediateResultManager` object which allows the application to tap into the algorithmic process.

| API Name                                                                            | Description                                     |
| ----------------------------------------------------------------------------------- | ----------------------------------------------- |
| [`getIntermediateResultManager`](intermediate-result.md#getintermediateresultmanager) | Returns an `IntermediateResultManager` object. |

## Auxiliary Methods

| Method                                      | Description                                               |
| --------------------------------------------- | --------------------------------------------------------- |
| [`setGlobalIntraOpNumThreads`](auxiliary-methods.md#setglobalintraopnumthreads) | Sets the global number of threads used internally for model execution. |
| [`appendDLModelBuffer`](auxiliary-methods.md#appenddlmodelbuffer) | Appends a deep learning model to the memory buffer. |
| [`clearDLModelBuffers`](auxiliary-methods.md#cleardlmodelbuffers) | Clears all deep learning models from buffer to free up memory. |
| [`appendModelBuffer`](auxiliary-methods.md#appendmodelbuffer) | Deprecated. Will be removed in future versions. Use `appendDLModelBuffer` instead. |
