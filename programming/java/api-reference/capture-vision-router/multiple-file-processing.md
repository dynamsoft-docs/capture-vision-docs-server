---
layout: default-layout
title: CaptureVisionRouter Multiple-File Processing Methods - Dynamsoft Capture Vision Router Module Java Edition API Reference
description: Definition of CaptureVisionRouter class Multiple-File Processing Methods in Dynamsoft Capture Vision Router Module Java Edition.
keywords: capture vision, multiple-file processing, api reference, java
needAutoGenerateSidebar: true
needGenerateH3Content: false
---

# Multiple-File Processing Methods - CaptureVisionRouter Class

| Method                                                              | Description                                                                  |
| ------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| [`setInput`](#setinput)                                             | Sets an image source to provide images for consecutive processing.         |
| [`getInput`](#getinput)                                             | Gets the attached image source adapter object of the capture vision router.         |
| [`addCaptureStateListener`](#addcapturestatelistener)               | Adds an object that listens to the state changes of the capture process.     |
| [`removeCaptureStateListener`](#removecapturestatelistener)         | Removes an object which listens to the state changes of the capture process. |
| [`addImageSourceStateListener`](#addimagesourcestatelistener)       | Adds an object that listens to state changes of the image source.            |
| [`removeImageSourceStateListener`](#removeimagesourcestatelistener) | Removes an object which listens to state changes of the image source.        |
| [`addResultReceiver`](#addresultreceiver)                           | Adds an object as the receiver of captured results.                          |
| [`removeResultReceiver`](#removeresultreceiver)                     | Removes an object which was added as a receiver of captured results.         |
| [`addResultFilter`](#addresultfilter)                               | Adds an object as the filter of captured results.                          |
| [`removeResultFilter`](#removeresultfilter)                         | Removes an object which was added as a filter of captured results.         |
| [`startCapturing`](#startcapturing)                                 | Starts to process images consecutively.                                      |
| [`stopCapturing`](#stopcapturing)                                   | Stops the consecutive processing.                                          |
| [`pauseCapturing`](#pausecapturing)                                 | Pauses the capture process. The current thread will be blocked until the capture process is resumed. |
| [`resumeCapturing`](#resumecapturing)                               | Resumes the capture process. The current thread will be unblocked after the capture process is resumed. |

## setInput

Sets an image source to provide images for consecutive processing.

```java
public void setInput(ImageSourceAdapter pAdapter) throws CaptureVisionException
```

**Parameters**

`pAdapter` Specifies an object which has implemented the `ImageSourceAdapter` interface.

**Exceptions**

[`CaptureVisionException`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-exception.html)

**See Also**

[ImageSourceAdapter]({{ site.dcvb_java_api }}core/basic-classes/image-source-adapter.html)

[DirectoryFetcher]({{ site.dcvb_java_api }}utility/directory-fetcher.html)

[FileFetcher]({{ site.dcvb_java_api }}utility/file-fetcher.html)

## getInput

Gets the attached image source adapter object of the capture vision router. 

```java
public ImageSourceAdapter getInput()
```

**Return Value**

Returns the attached image source adapter object of the capture vision router.

**See Also**

[ImageSourceAdapter]({{ site.dcvb_java_api }}core/basic-classes/image-source-adapter.html)

[DirectoryFetcher]({{ site.dcvb_java_api }}utility/directory-fetcher.html)

[FileFetcher]({{ site.dcvb_java_api }}utility/file-fetcher.html)

## addCaptureStateListener

Adds an object that listens to the state changes of the capture process.

```java
public void addCaptureStateListener(CaptureStateListener listener) throws CaptureVisionException
```

**Parameters**

`listener` Specifies a listening object of the type [`CaptureStateListener`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html) to be added.

**Exceptions**

[`CaptureVisionException`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-exception.html)

**See Also**

[CaptureStateListener]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)

## removeCaptureStateListener

Removes an object which listens to the state changes of the capture process.

```java
public void removeCaptureStateListener(CaptureStateListener listener) throws CaptureVisionException
```

**Parameters**

`listener` Specifies a listening object of the type [`CaptureStateListener`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html) to be removed.

**Exceptions**

[`CaptureVisionException`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-exception.html)

**See Also**

[CaptureStateListener]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)

## addImageSourceStateListener

Adds an object that listens to state changes of the image source.

```java
public void addImageSourceStateListener(ImageSourceStateListener listener) throws CaptureVisionException
```

**Parameters**

`listener` Specifies a listening object of the type [`ImageSourceStateListener`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html) to be added.

**Exceptions**

[`CaptureVisionException`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-exception.html)

**See Also**

[ImageSourceStateListener]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)

## removeImageSourceStateListener

Removes an object which listens to state changes of the image source.

```java
public void removeImageSourceStateListener(ImageSourceStateListener listener) throws CaptureVisionException
```

**Parameters**

`listener` Specifies a listening object of the type [`ImageSourceStateListener`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html) to be removed.

**Exceptions**

[`CaptureVisionException`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-exception.html)

**See Also**

[ImageSourceStateListener]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)

## addResultReceiver

Adds an object as the receiver of captured results.

```java
public void addResultReceiver(CapturedResultReceiver receiver) throws CaptureVisionException
```

**Parameters**

`receiver` Specifies a receiver object of the type [`CapturedResultReceiver`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) to be added.

**Exceptions**

[`CaptureVisionException`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-exception.html)

**See Also**

[CapturedResultReceiver]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html)

## removeResultReceiver

Removes an object which was added as a receiver of captured results.

```java
public void removeResultReceiver(CapturedResultReceiver receiver) throws CaptureVisionException
```

**Parameters**

`receiver` Specifies a receiver object of the type [`CapturedResultReceiver`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) to be removed.

**Exceptions**

[`CaptureVisionException`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-exception.html)

**See Also**

[CapturedResultReceiver]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html)

## addResultFilter

Adds an object as the filter of captured results.

```java
public void addResultFilter(CapturedResultFilter filter) throws CaptureVisionException
```

**Parameters**

`filter` Specifies a filter object of the type [`CapturedResultFilter`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html) to be added.

**Exceptions**

[`CaptureVisionException`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-exception.html)

**See Also**

[CapturedResultFilter]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html)

## removeResultFilter

Removes an object which was added as a filter of captured results.

```java
public void removeResultFilter(CapturedResultFilter filter)
```

**Parameters**

`filter` Specifies a filter object of the type [`CapturedResultFilter`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html) to be removed.

**See Also**

[CapturedResultFilter]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html)

## startCapturing

Starts to process images consecutively.

```java
public CaptureVisionError startCapturing() throws CaptureVisionException
public CaptureVisionError startCapturing(String templateName, boolean waitForThreadExit) throws CaptureVisionException
```

**Parameters**

`templateName` Specifies a `CaptureVisionTemplate` to use for capturing.

`waitForThreadExit` Indicates whether to wait for the capture process to complete before returning.

**Remarks**

- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_java_api }}capture-vision-router/enum-preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [initSettings]({{ site.dcvb_java_api }}capture-vision-router/settings.html#initsettings) / [initSettingsFromFile]({{ site.dcvb_java_api }}capture-vision-router/settings.html#initsettingsfromfile).
- When using a custom template, the parameter `templateName` should be the name of the [`CaptureVisionTemplate` object]({{ site.dcvb_parameters }}file/capture-vision-template.html) in the JSON template file.
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `initSettings` / `initSettingsFromFile` and pass his own settings.
- If parameter `templateName` is not specified, the preset one named 'Default' will be used. However, if the preset ones have been overwritten as described above, the first `CaptureVisionTemplate` from the user's own settings will be used instead.

**Return Value**

Returns a `CaptureVisionError` object that contains error information.

**Exceptions**

[`CaptureVisionException`]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-exception.html)

**See Also**

[CaptureVisionError]({{ site.dcvb_java_api }}capture-vision-router/auxiliary-classes/capture-vision-error.html)

## stopCapturing

Stops the multiple-file processing.

```java
public void stopCapturing()
public void stopCapturing(boolean waitForRemainingTasks, boolean waitForThreadExit)
```

**Parameters**

`waitForRemainingTasks` Indicates whether to wait for the remaining tasks to complete before returning. The default value is True.  
`waitForThreadExit` Indicates whether to wait for the capture process to complete before returning. The default value is True.

## pauseCapturing

Pauses the capture process. The current thread will be blocked until the capture process is resumed.

```java
public void pauseCapturing()
```

## resumeCapturing

Resumes the capture process. The current thread will be unblocked after the capture process is resumed.

```java
public void resumeCapturing()
```

