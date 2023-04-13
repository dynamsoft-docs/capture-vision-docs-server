---
layout: default-layout
title: CaptureVisionRouter Consecutive Process - Dynamsoft Capture Vision C++ Edition API
description: This page introduces APIs related to Consecutive Process of Dynamsoft Capture Vision C++ Edition.
keywords: capture vision, consecutive process, api reference, C++, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
permalink: /programming/cplusplus/api-reference/cvr/consecutive-process.html
---

# Capture Vision Router C++ API Reference - Consecutive Process

| API Name                                                            | Description                                                                  |
| ------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| [SetInput()](#setinput)                                             | Sets an image source to provide images for consecutive process.              |
| [AddCaptureStateListener()](#addcapturestatelistener)               | Adds an object that listens to the state changes of the capture process.     |
| [RemoveCaptureStateListener()](#removecapturestatelistener)         | Removes an object which listens to the state changes of the capture process. |
| [AddImageSourceStateListener()](#addimagesourcestatelistener)       | Adds an object that listens to state changes of the image source.            |
| [RemoveImageSourceStateListener()](#removeimagesourcestatelistener) | Removes an object which listens to state changes of the image source.        |
| [AddResultReceiver()](#addresultreceiver)                           | Adds an object as the receiver of captured results.                          |
| [RemoveResultReceiver()](#removeresultreceiver)                     | Removes an object which was added as a receiver of captured results.         |
| [StartCapturing()](#startcapturing)                                 | Starts to process images consecutively.                                      |
| [StopCapturing()](#stopcapturing)                                   | Stops the consecutive process.                                               |

## SetInput

Sets an image source to provide images for consecutive process.

```cpp
void SetInput(CImageSourceAdapter* pAdaptor);
```

### Parameters

| Name       | Description                                                                                                                    |
| ---------- | ------------------------------------------------------------------------------------------------------------------------------ |
| `pAdaptor` | Specifies an object which has implemented the [Image Source Adapter Interface]({{architecture}}input.md#image-source-adapter). |

### Return value

None.

### Code Snippet

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

### Parameters

| Name       | Description                                                                                                                      |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------- |
| `listener` | Specifies a listening object of the type [`CCaptureStateListener`](capture-state-listener.md#ccapturestatelistener) to be added. |

### Return value

None.

### Code Snippet

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

### Parameters

| Name       | Description                                                                                                                        |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| `listener` | Specifies a listening object of the type [`CCaptureStateListener`](capture-state-listener.md#ccapturestatelistener) to be removed. |

### Return value

None.

### Code Snippet

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

### Parameters

| Name       | Description                                                                                                                          |
| ---------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| `listener` | Specifies a listening object of the type [`CImageSourceStateListener`](capture-state-listener.md#ccapturestatelistener) to be added. |

### Return value

None.

### Code Snippet

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

### Parameters

| Name       | Description                                                                                                                            |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| `listener` | Specifies a listening object of the type [`CImageSourceStateListener`](capture-state-listener.md#ccapturestatelistener) to be removed. |

### Return value

None.

### Code Snippet

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

### Parameters

| Name       | Description                                                                                                                       |
| ---------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `receiver` | Specifies a receiver object of the type [`CCapturedResultReceiver`](capture-state-listener.md#ccapturestatelistener) to be added. |

### Return value

None.

### Code Snippet

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

### Parameters

| Name       | Description                                                                                                                         |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| `receiver` | Specifies a receiver object of the type [`CCapturedResultReceiver`](capture-state-listener.md#ccapturestatelistener) to be removed. |

### Return value

None.

### Code Snippet

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

### Parameters

| Name                | Description                                                                                                                               |
| ------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `templateName`      | Specifies a template to use for capturing. If no template is specified, an empty string is used which means the factory default template. |
| `waitForCompletion` | Indicates whether to wait for the capture process to complete before returning. The default value is false.                               |
| `errorMsgBuffer`    | Stores any error messages generated during the capturing process. If no buffer is provided, the error messages will not be output.        |
| `errorMsgBufferLen` | Specifies the length of the provided error message buffer. If no buffer is provided, this parameter is ignored.                           |

### Return value

The function returns an integer value representing the success or failure of the capturing process. A value of 0 indicates success, while a non-zero value indicates failure. If an error message buffer is provided, any error messages generated during the capturing process will be stored in the buffer.

### Code Snippet

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

Stops the consecutive process.

```cpp
void StopCapturing(bool waitForCompletion = true);
```

### Parameters

| Name                | Description                                                                                                 |
| ------------------- | ----------------------------------------------------------------------------------------------------------- |
| `waitForCompletion` | Indicates whether to wait for the capture process to complete before returning. The default value is false. |

### Return value

None.

### Code Snippet

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
