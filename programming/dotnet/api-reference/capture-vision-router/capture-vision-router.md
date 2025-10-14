---
layout: default-layout
title: CaptureVisionRouter Class- Dynamsoft Capture Vision Router Module .NET Edition API Reference
description: This page is about the CaptureVisionRouter Class of Dynamsoft Capture Vision Router Module .NET Edition.
keywords: capture vision router, router, .NET, api reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# CaptureVisionRouter

The `CaptureVisionRouter` class is what a user uses to interact with image-processing and semantic-processing products in their applications. It accepts an image source and returns processing results which may contain [Final results]({{site.dcvb_architecture}}output.html#final-results?lang=dotnet) or [Intermediate Results]({{site.dcvb_architecture}}output.html#intermediate-results?lang=dotnet).

## Definition

*Namespace:* Dynamsoft.CVR


```csharp
public class CaptureVisionRouter : IDisposable
```

## Constructor and Destructor Methods

| Method                                                           | Description                                           |
| ---------------------------------------------------------------- | ----------------------------------------------------- |
| [`CaptureVisionRouter`](instantiate.md#CaptureVisionRouter)    | Default constructor of `CaptureVisionRouter` object. |
| [`~CaptureVisionRouter`](instantiate.md#CaptureVisionRouter-1) | Destructor of `CaptureVisionRouter` object.          |
| [`Dispose`](instantiate.md#dispose) | Releases all resources used by current object. |

## Single-File Processing Methods

| Method                                         | Description                                               |
| ---------------------------------------------- | --------------------------------------------------------- |
| [`Capture`](single-file-processing.md#capture) | Processes an image or file to derive important information. |
| [`CaptureMultiPages`](single-file-processing.md#capturemultipages) | Processes an image or file containing multiple pages to derive important information. |

## Multiple-File Processing Methods

| Method                                                                                         | Description                                                                  |
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

## Setting Methods

| Method                                                       | Description                                                                                  |
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
| [`SwitchCapturingTemplate`](settings.md#switchcapturingtemplate)    | Switches the capturing template during the image processing workflow.                            |

## Auxiliary Methods

| Method                                      | Description                                               |
| --------------------------------------------- | --------------------------------------------------------- |
| [`GetBufferedItemsManager`](auxiliary-methods.md#getbuffereditemsmanager)                               | Gets the manager instance of buffered items. |
| [`GetIntermediateResultManager`](auxiliary-methods.md#getintermediateresultmanager) | Returns an `IntermediateResultManager` object. |
| [`SetGlobalIntraOpNumThreads`](auxiliary-methods.md#setglobalintraopnumthreads) | Sets the global number of threads used internally for model execution. |
| [`AppendDLModelBuffer`](auxiliary-methods.md#appenddlmodelbuffer) | Appends a deep learning model to the memory buffer. |
| [`ClearDLModelBuffers`](auxiliary-methods.md#cleardlmodelbuffers) | Clears all deep learning models from buffer to free up memory. |
| [`AppendModelBuffer`](auxiliary-methods.md#appendmodelbuffer) | Deprecated. Will be removed in future versions. Use `AppendDLModelBuffer` instead. |