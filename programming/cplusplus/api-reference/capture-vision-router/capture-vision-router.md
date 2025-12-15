---
layout: default-layout
title: Capture Vision Router Class- Dynamsoft Capture Vision C++ Edition API Reference
description: This page is about the Capture Vision Router Class of the C++ edition of the Dynamsoft Capture Vision Router Module.
keywords: capture vision router, router, c++, api reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: CVR C++ CCaptureVisionRouter Class
---

# CCaptureVisionRouter

The `CCaptureVisionRouter` class is what a user uses to interact with image-processing and semantic-processing products in their applications. It accepts an image source and returns processing results which may contain [Final results]({{site.dcvb_architecture}}output.html#final-results?lang=cpp) or [Intermediate Results]({{site.dcvb_architecture}}output.html#intermediate-results?lang=cpp).

## Definition

*Namespace:* dynamsoft::cvr

*Assembly:* DynamsoftCaptureVisionRouter

```cpp
class CCaptureVisionRouter
```

## Constructor and Destructor

| Method                                                           | Description                                           |
| ---------------------------------------------------------------- | ----------------------------------------------------- |
| [`CCaptureVisionRouter`](instantiate.md#ccapturevisionrouter)    | Default constructor of `CCaptureVisionRouter` object. |
| [`~CCaptureVisionRouter`](instantiate.md#ccapturevisionrouter-1) | Destructor of `CCaptureVisionRouter` object.          |

## Single-File Processing

| API Name                                       | Description                                               |
| ---------------------------------------------- | --------------------------------------------------------- |
| [`Capture`](single-file-processing.md#capture) | Processes an image or file to derive important information. |
| [`CaptureMultiPages`](single-file-processing.md#capturemultipages) | Processes an image or file containing multiple pages to derive important information. |

## Multiple-File Processing

| API Name                                                                                       | Description                                                                  |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| [`SetInput`](multiple-file-processing.md#setinput)                                             | Sets an image source to provide images for consecutive process.              |
| [`GetInput`](multiple-file-processing.md#getinput)                                             | Gets the attached image source adapter object of the capture vision router.  |
| [`AddCaptureStateListener`](multiple-file-processing.md#addcapturestatelistener)               | Adds an object that listens to the state changes of the capture process.     |
| [`RemoveCaptureStateListener`](multiple-file-processing.md#removecapturestatelistener)         | Removes an object which listens to the state changes of the capture process. |
| [`AddImageSourceStateListener`](multiple-file-processing.md#addimagesourcestatelistener)       | Adds an object that listens to state changes of the image source.            |
| [`RemoveImageSourceStateListener`](multiple-file-processing.md#removeimagesourcestatelistener) | Removes an object which listens to state changes of the image source.        |
| [`AddResultReceiver`](multiple-file-processing.md#addresultreceiver)                           | Adds an object as the receiver of captured results.                          |
| [`RemoveResultReceiver`](multiple-file-processing.md#removeresultreceiver)                     | Removes an object which was added as a receiver of captured results.         |
| [`AddResultFilter`](multiple-file-processing.md#addresultfilter)                               | Adds an object as the filter of captured results.                            |
| [`RemoveResultFilter`](multiple-file-processing.md#removeresultfilter)                         | Removes an object which was added as a filter of captured results.           |
| [`StartCapturing`](multiple-file-processing.md#startcapturing)                                 | Starts to process images consecutively.                                      |
| [`StopCapturing`](multiple-file-processing.md#stopcapturing)                                   | Stops the consecutive process.                                               |
| [`PauseCapturing`](multiple-file-processing.md#pausecapturing)                                 | Pauses the capture process. The current thread will be blocked until the capture process is resumed. |
| [`ResumeCapturing`](multiple-file-processing.md#resumecapturing)                               | Resumes the capture process. The current thread will be unblocked after the capture process is resumed. |
| [`SwitchCapturingTemplate`](multiple-file-processing.md#switchcapturingtemplate)    | Switches the capturing template during the image processing workflow.                            |

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
| [`GetParameterTemplateCount`](settings.md#getparametertemplatecount)  | Retrieves the total number of available parameter templates.                                 |
| [`GetParameterTemplateName`](settings.md#getparametertemplatename)    | Retrieves the name of a specific parameter template by its index.                            |

## Intermediate Result

The following method returns an `CIntermediateResultManager` object which allows the application to tap into the algorithmic process.

| API Name                                                                            | Description                                     |
| ----------------------------------------------------------------------------------- | ----------------------------------------------- |
| [`GetIntermediateResultManager`](intermediate-result.md#getintermediateresultmanager) | Returns an `CIntermediateResultManager` object. |

## Buffered Items

| API Name                                                     | Description                                                                                  |
| ------------------------------------------------------------ | -------------------------------------------------------------------------------------------- |
| [`GetBufferedItemsManager`](buffered-items.md#getbuffereditemsmanager)                               | Gets the manager instance of buffered items. |

## Auxiliary

| API Name                                      | Description                                               |
| --------------------------------------------- | --------------------------------------------------------- |
| [`FreeString`](auxiliary-methods.md#freestring) | The function is *deprecated*, use [`CoreModule::FreeBytes`]({{ site.dcvb_cpp_api }}core/basic-structures/core-module.html#freebytes) instead.                 |
| [`SetGlobalIntraOpNumThreads`](auxiliary-methods.md#setglobalintraopnumthreads) | Sets the global number of threads used internally for model execution. |
| [`AppendDLModelBuffer`](auxiliary-methods.md#appenddlmodelbuffer) | Appends a deep learning model to the memory buffer. |
| [`ClearDLModelBuffers`](auxiliary-methods.md#cleardlmodelbuffers) | Clears all deep learning models from buffer to free up memory. |
| [`AppendModelBuffer`](auxiliary-methods.md#appendmodelbuffer) | Deprecated. Will be removed in future versions. Use `AppendDLModelBuffer` instead. |
