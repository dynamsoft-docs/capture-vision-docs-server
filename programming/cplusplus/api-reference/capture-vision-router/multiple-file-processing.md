---
layout: default-layout
title: CaptureVisionRouter Multiple-File Processing - Dynamsoft Capture Vision C++ Edition API
description: This page introduces APIs related to "Multiple-File Processing" by the CCaptureVisionRouter class of the Dynamsoft Capture Vision C++ Edition.
keywords: capture vision, multiple-file processing, api reference, C++
needAutoGenerateSidebar: true
needGenerateH3Content: false
breadcrumbText: CVR C++ Multiple-File Processing
permalink: /programming/cplusplus/api-reference/capture-vision-router/multiple-file-processing.html
---

# Capture Vision Router C++ API Reference - Multiple-File Processing

| API Name                                                            | Description                                                                  |
| ------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| [SetInput()](#setinput)                                             | Sets an image source to provide images for consecutive processing.         |
| [AddCaptureStateListener()](#addcapturestatelistener)               | Adds an object that listens to the state changes of the capture process.     |
| [RemoveCaptureStateListener()](#removecapturestatelistener)         | Removes an object which listens to the state changes of the capture process. |
| [AddImageSourceStateListener()](#addimagesourcestatelistener)       | Adds an object that listens to state changes of the image source.            |
| [RemoveImageSourceStateListener()](#removeimagesourcestatelistener) | Removes an object which listens to state changes of the image source.        |
| [AddResultReceiver()](#addresultreceiver)                           | Adds an object as the receiver of captured results.                          |
| [RemoveResultReceiver()](#removeresultreceiver)                     | Removes an object which was added as a receiver of captured results.         |
| [StartCapturing()](#startcapturing)                                 | Starts to process images consecutively.                                      |
| [StopCapturing()](#stopcapturing)                                   | Stops the consecutive processing.                                          |

## SetInput

Sets an image source to provide images for consecutive processing.

```cpp
void SetInput(CImageSourceAdapter* pAdaptor);
```

**Parameters**

`[in] pAdaptor` Specifies an object which has implemented the [Image Source Adapter Interface]({{architecture}}input.md#image-source-adapter).

**Return Value**

None.

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

## AddCaptureStateListener

Adds an object that listens to the state changes of the capture process.

```cpp
void AddCaptureStateListener(CCaptureStateListener* listener);
```

**Parameters**

`[in] listener` Specifies a listening object of the type [`CCaptureStateListener`](capture-state-listener.md#ccapturestatelistener) to be added.

**Return Value**

None.

**Code Snippet**

```cpp
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
CCaptureVisionRouter* router = new CCaptureVisionRouter();
CCaptureStateListener* listener = new CCaptureStateListener();
router->AddCaptureStateListener(listener);
//...
delete router;
```

## RemoveCaptureStateListener

Removes an object which listens to the state changes of the capture process.

```cpp
void RemoveCaptureStateListener(CCaptureStateListener* listener);
```

**Parameters**

`[in] listener` Specifies a listening object of the type [`CCaptureStateListener`](capture-state-listener.md#ccapturestatelistener) to be removed.

**Return Value**

None.

**Code Snippet**

```cpp
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
CCaptureVisionRouter* router = new CCaptureVisionRouter();
CCaptureStateListener* listener = new CCaptureStateListener();
router->AddCaptureStateListener(listener);
//...
router->RemoveCaptureStateListener(listener);
delete router;
```

## AddImageSourceStateListener

Adds an object that listens to state changes of the image source.

```cpp
void AddImageSourceStateListener(CImageSourceStateListener* listener);
```

**Parameters**

`[in] listener` Specifies a listening object of the type [`CImageSourceStateListener`](capture-state-listener.md#ccapturestatelistener) to be added.

**Return Value**

None.

**Code Snippet**

```cpp
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
CCaptureVisionRouter* router = new CCaptureVisionRouter();
CImageSourceStateListener* listener = new CImageSourceStateListener();
router->AddImageSourceStateListener(listener);
//...
delete router;
```

## RemoveImageSourceStateListener

Removes an object which listens to state changes of the image source.

```cpp
void RemoveImageSourceStateListener(CImageSourceStateListener* listener);
```

**Parameters**

`[in] listener` Specifies a listening object of the type [`CImageSourceStateListener`](capture-state-listener.md#ccapturestatelistener) to be removed.

**Return Value**

None.

**Code Snippet**

```cpp
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
CCaptureVisionRouter* router = new CCaptureVisionRouter();
CImageSourceStateListener* listener = new CImageSourceStateListener();
router->AddImageSourceStateListener(listener);
//...
router->RemoveImageSourceStateListener(listener);
delete router;
```

## AddResultReceiver

Adds an object as the receiver of captured results.

```cpp
void AddResultReceiver(CCapturedResultReceiver* receiver);
```

**Parameters**

`[in] receiver` Specifies a receiver object of the type [`CCapturedResultReceiver`](capture-state-listener.md#ccapturestatelistener) to be added.

**Return Value**

None.

**Code Snippet**

```cpp
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
CCaptureVisionRouter* router = new CCaptureVisionRouter();
CCapturedResultReceiver* receiver = new CCapturedResultReceiver();
router->AddResultReceiver(receiver);
//...
delete router;
```

## RemoveResultReceiver

Removes an object which was added as a receiver of captured results.

```cpp
void RemoveResultReceiver(CCapturedResultReceiver* receiver);
```

**Parameters**

`[in] receiver` Specifies a receiver object of the type [`CCapturedResultReceiver`](capture-state-listener.md#ccapturestatelistener) to be removed.

**Return Value**

None.

**Code Snippet**

```cpp
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
CCaptureVisionRouter* router = new CCaptureVisionRouter();
CCapturedResultReceiver* receiver = new CCapturedResultReceiver();
router->AddResultReceiver(receiver);
//...
router->RemoveResultReceiver(receiver);
delete router;
```

## StartCapturing

Starts to process images consecutively.

```cpp
int StartCapturing(const char* templateName = "", bool waitForCompletion = false, char errorMsgBuffer[]=NULL, const int errorMsgBufferLen=0);
```

**Parameters**

`[in] templateName` Specifies a template to use for capturing. If not specified, an empty string is used which means the factory default template.

`[in] waitForCompletion` Indicates whether to wait for the capture process to complete before returning. The default value is false.

`[out] errorMsgBuffer` Stores any error messages generated during the capturing process. If no buffer is provided, the error messages will not be output.

`[in] errorMsgBufferLen` Specifies the length of the provided error message buffer. If no buffer is provided, this parameter is ignored.

**Return Value**

The function returns an integer value representing the success or failure of the capturing process. A value of 0 indicates success, while a non-zero value indicates failure. If an error message buffer is provided, any error messages generated during the capturing process will be stored in the buffer.

**Code Snippet**

```cpp
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
CCaptureVisionRouter* router = new CCaptureVisionRouter();
char szErrorMsg2[256];
router->StartCapturing("myTemplate", true, szErrorMsg2, 256);
//...
delete router;
```

## StopCapturing()

Stops the multiple-file processing.

```cpp
void StopCapturing(bool waitForCompletion = true);
```

**Parameters**

`[in] waitForCompletion` Indicates whether to wait for the capture process to complete before returning. The default value is false.

**Return Value**

None.

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