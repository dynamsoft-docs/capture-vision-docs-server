---
layout: default-layout
title: CaptureVisionRouter Multiple-File Processing - Dynamsoft Capture Vision C++ Edition API
description: This page introduces APIs related to Multiple-File Processing by the CCaptureVisionRouter class of the Dynamsoft Capture Vision C++ Edition.
keywords: capture vision, multiple-file processing, api reference, C++
needAutoGenerateSidebar: true
needGenerateH3Content: false
breadcrumbText: CVR C++ Multiple-File Processing
permalink: /programming/cplusplus/api-reference/capture-vision-router/multiple-file-processing.html
---

# Multiple-File Processing

| API Name                                                            | Description                                                                  |
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

```cpp
int SetInput(CImageSourceAdapter* pAdaptor);
```

**Parameters**

`[in] pAdaptor` Specifies an object which has implemented the [Image Source Adapter Interface]({{site.architecture}}input.html#image-source-adapter).

**Return Value**

Returns an error code. Zero indicates success.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

**Code Snippet**

```cpp
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
CCaptureVisionRouter* router = new CCaptureVisionRouter();
CDirectoryFetcher* fetcher = new CDirectoryFetcher();
router->SetInput(fetcher);
//...
delete router;
```

**See Also**

[CImageSourceAdapter]({{ site.dcv_cpp_api }}core/basic-structures/image-source-adapter.html)

[CDirectoryFetcher]({{ site.dcv_cpp_api }}utility/directory-fetcher.html)

[CFileFetcher]({{ site.dcv_cpp_api }}utility/file-fetcher.html)

## GetInput

Gets the attached image source adapter object of the capture vision router. 

```cpp
CImageSourceAdapter* GetInput();
```

**Return Value**

Returns the attached image source adapter object of the capture vision router.

**Code Snippet**

```cpp
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
CCaptureVisionRouter* router = new CCaptureVisionRouter();
CDirectoryFetcher* fetcher = new CDirectoryFetcher();
router->SetInput(fetcher);
CImageSourceAdapter* input = router->GetInput();
//...
delete router;
```

**See Also**

[CImageSourceAdapter]({{ site.dcv_cpp_api }}core/basic-structures/image-source-adapter.html)

[CDirectoryFetcher]({{ site.dcv_cpp_api }}utility/directory-fetcher.html)

[CFileFetcher]({{ site.dcv_cpp_api }}utility/file-fetcher.html)

## AddCaptureStateListener

Adds an object that listens to the state changes of the capture process.

```cpp
int AddCaptureStateListener(CCaptureStateListener* listener);
```

**Parameters**

`[in] listener` Specifies a listening object of the type [`CCaptureStateListener`](./auxiliary-classes/capture-state-listener.md#ccapturestatelistener) to be added.

**Return Value**

Returns an error code. Zero indicates success.

**Code Snippet**

```cpp
class MyCaptureStateListener: public CCaptureStateListener
{
public:
    void OnCaptureStateChanged(CaptureState state) {
        // user code...
    }
};
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
CCaptureVisionRouter* router = new CCaptureVisionRouter();
CCaptureStateListener* listener = new MyCaptureStateListener();
router->AddCaptureStateListener(listener);
//...
delete router;
```

**See Also**

[CCaptureStateListener]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)

## RemoveCaptureStateListener

Removes an object which listens to the state changes of the capture process.

```cpp
int RemoveCaptureStateListener(CCaptureStateListener* listener);
```

**Parameters**

`[in] listener` Specifies a listening object of the type [`CCaptureStateListener`](./auxiliary-classes/capture-state-listener.md#ccapturestatelistener) to be removed.

**Return Value**

Returns an error code. Zero indicates success.

**Code Snippet**

```cpp
class MyCaptureStateListener: public CCaptureStateListener
{
public:
    void OnCaptureStateChanged(CaptureState state) {
        // user code...
    }
};
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
CCaptureVisionRouter* router = new CCaptureVisionRouter();
CCaptureStateListener* listener = new MyCaptureStateListener();
router->AddCaptureStateListener(listener);
//...
router->RemoveCaptureStateListener(listener);
delete router;
```

**See Also**

[CCaptureStateListener]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)

## AddImageSourceStateListener

Adds an object that listens to state changes of the image source.

```cpp
int AddImageSourceStateListener(CImageSourceStateListener* listener);
```

**Parameters**

`[in] listener` Specifies a listening object of the type [`CImageSourceStateListener`](./auxiliary-classes/image-source-state-listener.md) to be added.

**Return Value**

Returns an error code. Zero indicates success.

**Code Snippet**

```cpp
class CMyImageSourceStateListener: public CImageSourceStateListener
{
public:
    void OnImageSourceStateReceived(ImageSourceState state) {
        // user code...
    }
};
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
CCaptureVisionRouter* router = new CCaptureVisionRouter();
CImageSourceStateListener* listener = new CMyImageSourceStateListener();
router->AddImageSourceStateListener(listener);
//...
delete router;
```

**See Also**

[CImageSourceStateListener]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)

## RemoveImageSourceStateListener

Removes an object which listens to state changes of the image source.

```cpp
int RemoveImageSourceStateListener(CImageSourceStateListener* listener);
```

**Parameters**

`[in] listener` Specifies a listening object of the type [`CImageSourceStateListener`](./auxiliary-classes/image-source-state-listener.md) to be removed.

**Return Value**

Returns an error code. Zero indicates success.

**Code Snippet**

```cpp
class CMyImageSourceStateListener: public CImageSourceStateListener
{
public:
    void OnImageSourceStateReceived(ImageSourceState state) {
        // user code...
    }
};
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
CCaptureVisionRouter* router = new CCaptureVisionRouter();
CImageSourceStateListener* listener = new CMyImageSourceStateListener();
router->AddImageSourceStateListener(listener);
//...
router->RemoveImageSourceStateListener(listener);
delete router;
```

**See Also**

[CImageSourceStateListener]({{ site.dcv_cpp_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)

## AddResultReceiver

Adds an object as the receiver of captured results.

```cpp
int AddResultReceiver(CCapturedResultReceiver* receiver);
```

**Parameters**

`[in] receiver` Specifies a receiver object of the type [`CCapturedResultReceiver`](../core/basic-structures/captured-result-receiver.md) to be added.

**Return Value**

Returns an error code. Zero indicates success.

**Code Snippet**

```cpp
class MyResultReceiver: public CCapturedResultReceiver
{
public:
    void OnCapturedResultReceived(const CCapturedResult* result) {
        // user code...
    }
};
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
CCaptureVisionRouter* router = new CCaptureVisionRouter();
CCapturedResultReceiver* receiver = new MyResultReceiver();
router->AddResultReceiver(receiver);
//...
delete router;
```

**See Also**

[CCapturedResultReceiver]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-receiver.html)

## RemoveResultReceiver

Removes an object which was added as a receiver of captured results.

```cpp
int RemoveResultReceiver(CCapturedResultReceiver* receiver);
```

**Parameters**

`[in] receiver` Specifies a receiver object of the type [`CCapturedResultReceiver`](../core/basic-structures/captured-result-receiver.md) to be removed.

**Return Value**

Returns an error code. Zero indicates success.

**Code Snippet**

```cpp
class MyResultReceiver: public CCapturedResultReceiver
{
public:
    void OnCapturedResultReceived(const CCapturedResult* result) {
        // user code...
    }
};
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
CCaptureVisionRouter* router = new CCaptureVisionRouter();
CCapturedResultReceiver* receiver = new MyResultReceiver();
router->AddResultReceiver(receiver);
//...
router->RemoveResultReceiver(receiver);
delete router;
```

**See Also**

[CCapturedResultReceiver]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-receiver.html)

## AddResultFilter

Adds an object as the filter of captured results.

```cpp
int AddResultFilter(CCapturedResultFilter* filter);
```

**Parameters**

`[in] filter` Specifies a filter object of the type [`CCapturedResultFilter`](../core/basic-structures/captured-result-filter.md) to be added.

**Return Value**

Returns an error code. Zero indicates success.

**Code Snippet**

```cpp
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
CCaptureVisionRouter* router = new CCaptureVisionRouter();
CCapturedResultFilter* filter = new CMultiFrameResultCrossFilter();
router->AddResultFilter(filter);
//...
delete router;
```

**See Also**

[CCapturedResultFilter]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-filter.html)

## RemoveResultFilter

Removes an object which was added as a filter of captured results.

```cpp
int RemoveResultFilter(CCapturedResultFilter* filter);
```

**Parameters**

`[in] filter` Specifies a filter object of the type [`CCapturedResultFilter`](../core/basic-structures/captured-result-filter.md) to be removed.

**Return Value**

Returns an error code. Zero indicates success.

**Code Snippet**

```cpp
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
CCaptureVisionRouter* router = new CCaptureVisionRouter();
CCapturedResultFilter* filter = new CMultiFrameResultCrossFilter();
router->AddResultFilter(filter);
//...
router->RemoveResultFilter(filter);
delete router;
```

**See Also**

[CCapturedResultFilter]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-filter.html)

## StartCapturing

Starts to process images consecutively.

```cpp
int StartCapturing(const char* templateName = "", bool waitForThreadExit = false, char errorMsgBuffer[]=NULL, const int errorMsgBufferLen=0);
```

**Parameters**

`[in] templateName` Specifies a template to use for capturing. If not specified, an empty string is used which means the factory default template.

`[in] waitForThreadExit` Indicates whether to wait for the capture process to complete before returning. The default value is false.

`[out] errorMsgBuffer` Stores any error messages generated during the capturing process. If no buffer is provided, the error messages will not be output.

`[in] errorMsgBufferLen` Specifies the length of the provided error message buffer. If no buffer is provided, this parameter is ignored.

**Return Value**

The function returns an integer value representing the success or failure of the capturing process. A value of 0 indicates success, while a non-zero value indicates failure. If an error message buffer is provided, any error messages generated during the capturing process will be stored in the buffer.

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_NO_IMAGE_SOURCE | -10063 | Can not start capturing before you set the input. |

**Code Snippet**

```cpp
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
CCaptureVisionRouter* router = new CCaptureVisionRouter();
router->StartCapturing("myTemplate", true, szErrorMsg, 256);
//...
delete router;
```

## StopCapturing

Stops the multiple-file processing.

```cpp
void StopCapturing(bool waitForRemainingTasks = true, bool waitForThreadExit = false);
```

**Parameters**

`[in] waitForRemainingTasks` Indicates whether to wait for the remaining tasks to complete before returning. The default value is true.  
`[in] waitForThreadExit` Indicates whether to wait for the capture process to complete before returning. The default value is false.

**Code Snippet**

```cpp
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
CCaptureVisionRouter* router = new CCaptureVisionRouter();
char szErrorMsg2[256];
router->StartCapturing("myTemplate", true, szErrorMsg2, 256);
//...
router->StopCapturing(true);
delete router;
```

## PauseCapturing

Pauses the capture process. The current thread will be blocked until the capture process is resumed.

```cpp
void PauseCapturing();
```

## ResumeCapturing

Resumes the capture process. The current thread will be unblocked after the capture process is resumed.

```cpp
void ResumeCapturing();
```
