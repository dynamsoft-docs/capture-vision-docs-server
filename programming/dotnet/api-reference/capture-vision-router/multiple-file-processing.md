---
layout: default-layout
title: CaptureVisionRouter Multiple-File Processing Methods - Dynamsoft Capture Vision Router Module .NET Edition API Reference
description: Definition of CaptureVisionRouter class Multiple-File Processing Methods in Dynamsoft Capture Vision Router Module .NET Edition.
keywords: capture vision, multiple-file processing, api reference, .NET
needAutoGenerateSidebar: true
needGenerateH3Content: false
---

# Multiple-File Processing Methods - CaptureVisionRouter Class

| Method                                                              | Description                                                                  |
| ------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| [`SetInput`](#setinput)                                             | Sets an image source to provide images for consecutive processing.         |
| [`GetInput`](#getinput)                                             | Gets the attached image source adapter object of the capture vision router.         |
| [`AddCaptureStateListener`](#addcapturestatelistener)               | Adds an object that listens to the state changes of the capture process.     |
| [`RemoveCaptureStateListener`](#removecapturestatelistener)         | Removes an object which listens to the state changes of the capture process. |
| [`AddImageSourceStateListener`](#addimagesourcestatelistener)       | Adds an object that listens to state changes of the image source.            |
| [`RemoveImageSourceStateListener`](#removeimagesourcestatelistener) | Removes an object which listens to state changes of the image source.        |
| [`AddResultReceiver`](#addresultreceiver)                           | Adds an object as the receiver of captured results.                          |
| [`RemoveResultReceiver`](#removeresultreceiver)                     | Removes an object which was added as a receiver of captured results.         |
| [`AddResultFilter`](#addresultfilter)                               | Adds an object as the filter of captured results.                          |
| [`RemoveResultFilter`](#removeresultfilter)                         | Removes an object which was added as a filter of captured results.         |
| [`StartCapturing`](#startcapturing)                                 | Starts to process images consecutively.                                      |
| [`StopCapturing`](#stopcapturing)                                   | Stops the consecutive processing.                                          |
| [`PauseCapturing`](#pausecapturing)                                 | Pauses the capture process. The current thread will be blocked until the capture process is resumed. |
| [`ResumeCapturing`](#resumecapturing)                               | Resumes the capture process. The current thread will be unblocked after the capture process is resumed. |

## SetInput

Sets an image source to provide images for consecutive processing.

```csharp
int SetInput(ImageSourceAdapter pAdaptor)
```

**Parameters**

`[in] pAdaptor` Specifies an object which has implemented the [Image Source Adapter Interface]({{site.dcv_architecture}}input.html#image-source-adapter).

**Return Value**

Returns an error code. Zero indicates success.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

**See Also**

[ImageSourceAdapter]({{ site.dcv_dotnet_api }}core/basic-classes/image-source-adapter.html)

[DirectoryFetcher]({{ site.dcv_dotnet_api }}utility/directory-fetcher.html)

[FileFetcher]({{ site.dcv_dotnet_api }}utility/file-fetcher.html)

## GetInput

Gets the attached image source adapter object of the capture vision router. 

```csharp
ImageSourceAdapter GetInput()
```

**Return Value**

Returns the attached image source adapter object of the capture vision router.

**See Also**

[ImageSourceAdapter]({{ site.dcv_dotnet_api }}core/basic-classes/image-source-adapter.html)

[DirectoryFetcher]({{ site.dcv_dotnet_api }}utility/directory-fetcher.html)

[FileFetcher]({{ site.dcv_dotnet_api }}utility/file-fetcher.html)

## AddCaptureStateListener

Adds an object that listens to the state changes of the capture process.

```csharp
int AddCaptureStateListener(ICaptureStateListener listener)
```

**Parameters**

`[in] listener` Specifies a listening object of the type [`ICaptureStateListener`]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html) to be added.

**Return Value**

Returns an error code. Zero indicates success.

**See Also**

[ICaptureStateListener]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)

## RemoveCaptureStateListener

Removes an object which listens to the state changes of the capture process.

```csharp
int RemoveCaptureStateListener(ICaptureStateListener listener)
```

**Parameters**

`[in] listener` Specifies a listening object of the type [`ICaptureStateListener`]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html) to be removed.

**Return Value**

Returns an error code. Zero indicates success.

**See Also**

[ICaptureStateListener]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)

## AddImageSourceStateListener

Adds an object that listens to state changes of the image source.

```csharp
int AddImageSourceStateListener(IImageSourceStateListener listener)
```

**Parameters**

`[in] listener` Specifies a listening object of the type [`IImageSourceStateListener`]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html) to be added.

**Return Value**

Returns an error code. Zero indicates success.

**See Also**

[IImageSourceStateListener]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)

## RemoveImageSourceStateListener

Removes an object which listens to state changes of the image source.

```csharp
int RemoveImageSourceStateListener(IImageSourceStateListener listener)
```

**Parameters**

`[in] listener` Specifies a listening object of the type [`IImageSourceStateListener`]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html) to be removed.

**Return Value**

Returns an error code. Zero indicates success.

**See Also**

[IImageSourceStateListener]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)

## AddResultReceiver

Adds an object as the receiver of captured results.

```csharp
int AddResultReceiver(CapturedResultReceiver receiver)
```

**Parameters**

`[in] receiver` Specifies a receiver object of the type [`CapturedResultReceiver`]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) to be added.

**Return Value**

Returns an error code. Zero indicates success.

**See Also**

[CapturedResultReceiver]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html)

## RemoveResultReceiver

Removes an object which was added as a receiver of captured results.

```csharp
int RemoveResultReceiver(CapturedResultReceiver receiver)
```

**Parameters**

`[in] receiver` Specifies a receiver object of the type [`CapturedResultReceiver`]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) to be removed.

**Return Value**

Returns an error code. Zero indicates success.

**See Also**

[CapturedResultReceiver]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html)

## AddResultFilter

Adds an object as the filter of captured results.

```csharp
int AddResultFilter(CapturedResultFilter filter)
```

**Parameters**

`[in] filter` Specifies a filter object of the type [`CapturedResultFilter`]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html) to be added.

**Return Value**

Returns an error code. Zero indicates success.

**See Also**

[CapturedResultFilter]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html)

## RemoveResultFilter

Removes an object which was added as a filter of captured results.

```csharp
int RemoveResultFilter(CapturedResultFilter filter)
```

**Parameters**

`[in] filter` Specifies a filter object of the type [`CapturedResultFilter`]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html) to be removed.

**Return Value**

Returns an error code. Zero indicates success.

**See Also**

[CapturedResultFilter]({{ site.dcv_dotnet_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html)

## StartCapturing

Starts to process images consecutively.

```csharp
int StartCapturing(string templateName, bool waitForThreadExit, out string errorMsgBuffer)
```

**Parameters**

`[in] templateName` Specifies a template to use for capturing. Setting an empty string means the factory default template.

`[in] waitForThreadExit` Indicates whether to wait for the capture process to complete before returning.

`[out] errorMsgBuffer` Stores any error messages generated during the capturing process.

**Return Value**

The function returns an integer value representing the success or failure of the capturing process. A value of 0 indicates success, while a non-zero value indicates failure. Any error messages generated during the capturing process will be returned in `errorMsgBuffer`.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_NO_IMAGE_SOURCE | -10063 | Can not start capturing before you set the input. |

## StopCapturing

Stops the multiple-file processing.

```csharp
void StopCapturing(bool waitForRemainingTasks = true, bool waitForThreadExit = false)
```

**Parameters**

`[in] waitForRemainingTasks` Indicates whether to wait for the remaining tasks to complete before returning. The default value is true.  
`[in] waitForThreadExit` Indicates whether to wait for the capture process to complete before returning. The default value is false.


## PauseCapturing

Pauses the capture process. The current thread will be blocked until the capture process is resumed.

```csharp
void PauseCapturing()
```

## ResumeCapturing

Resumes the capture process. The current thread will be unblocked after the capture process is resumed.

```csharp
void ResumeCapturing()
```

