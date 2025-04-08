---
layout: default-layout
title: CaptureVisionRouter Multiple-File Processing Methods - Dynamsoft Capture Vision Router Module Python Edition API Reference
description: Definition of CaptureVisionRouter class Multiple-File Processing Methods in Dynamsoft Capture Vision Router Module Python Edition.
keywords: capture vision, multiple-file processing, api reference, python
needAutoGenerateSidebar: true
needGenerateH3Content: false
---

# Multiple-File Processing Methods - CaptureVisionRouter Class

| Method                                                              | Description                                                                  |
| ------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| [`set_input`](#set_input)                                             | Sets an image source to provide images for consecutive processing.         |
| [`get_input`](#get_input)                                             | Gets the attached image source adapter object of the capture vision router.         |
| [`add_capture_state_listener`](#add_capture_state_listener)               | Adds an object that listens to the state changes of the capture process.     |
| [`remove_capture_state_listener`](#remove_capture_state_listener)         | Removes an object which listens to the state changes of the capture process. |
| [`add_image_source_state_listener`](#add_image_source_state_listener)       | Adds an object that listens to state changes of the image source.            |
| [`remove_image_source_state_listener`](#remove_image_source_state_listener) | Removes an object which listens to state changes of the image source.        |
| [`add_result_receiver`](#add_result_receiver)                           | Adds an object as the receiver of captured results.                          |
| [`remove_result_receiver`](#remove_result_receiver)                     | Removes an object which was added as a receiver of captured results.         |
| [`add_result_filter`](#add_result_filter)                               | Adds an object as the filter of captured results.                          |
| [`remove_result_filter`](#remove_result_filter)                         | Removes an object which was added as a filter of captured results.         |
| [`start_capturing`](#start_capturing)                                 | Starts to process images consecutively.                                      |
| [`stop_capturing`](#stop_capturing)                                   | Stops the consecutive processing.                                          |
| [`pause_capturing`](#pause_capturing)                                 | Pauses the capture process. The current thread will be blocked until the capture process is resumed. |
| [`resume_capturing`](#resume_capturing)                               | Resumes the capture process. The current thread will be unblocked after the capture process is resumed. |

## set_input

Sets an image source to provide images for consecutive processing.

```python
def set_input(self, adapter: ImageSourceAdapter) -> Tuple[int, str]:
```

**Parameters**

`adapter` Specifies an object which has implemented the `ImageSourceAdapter` Class.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html?lang=python)

[ImageSourceAdapter]({{ site.dcvb_python_api }}core/basic-classes/image-source-adapter.html)

[DirectoryFetcher]({{ site.dcvb_python_api }}utility/directory-fetcher.html)

[FileFetcher]({{ site.dcvb_python_api }}utility/file-fetcher.html)

## get_input

Gets the attached image source adapter object of the capture vision router. 

```python
def get_input(self) -> ImageSourceAdapter:
```

**Return Value**

Returns the attached image source adapter object of the capture vision router.

**See Also**

[ImageSourceAdapter]({{ site.dcvb_python_api }}core/basic-classes/image-source-adapter.html)

[DirectoryFetcher]({{ site.dcvb_python_api }}utility/directory-fetcher.html)

[FileFetcher]({{ site.dcvb_python_api }}utility/file-fetcher.html)

## add_capture_state_listener

Adds an object that listens to the state changes of the capture process.

```python
def add_capture_state_listener(self, listener: CaptureStateListener) -> Tuple[int, str]:
```

**Parameters**

`listener` Specifies a listening object of the type [`CaptureStateListener`]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html) to be added.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html?lang=python)

[CaptureStateListener]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)

## remove_capture_state_listener

Removes an object which listens to the state changes of the capture process.

```python
def remove_capture_state_listener(self, listener: CaptureStateListener) -> Tuple[int, str]:
```

**Parameters**

`listener` Specifies a listening object of the type [`CaptureStateListener`]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html) to be removed.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html?lang=python)

[CaptureStateListener]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)

## add_image_source_state_listener

Adds an object that listens to state changes of the image source.

```python
def add_image_source_state_listener(self, listener: ImageSourceStateListener) -> Tuple[int, str]:
```

**Parameters**

`listener` Specifies a listening object of the type [`ImageSourceStateListener`]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html) to be added.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html?lang=python)

[ImageSourceStateListener]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)

## remove_image_source_state_listener

Removes an object which listens to state changes of the image source.

```python
def remove_image_source_state_listener(self, listener: ImageSourceStateListener) -> Tuple[int, str]:
```

**Parameters**

`listener` Specifies a listening object of the type [`ImageSourceStateListener`]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html) to be removed.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html?lang=python)

[ImageSourceStateListener]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)

## add_result_receiver

Adds an object as the receiver of captured results.

```python
def add_result_receiver(self, receiver: CapturedResultReceiver) -> Tuple[int, str]:
```

**Parameters**

`receiver` Specifies a receiver object of the type [`CapturedResultReceiver`]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) to be added.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html?lang=python)

[CapturedResultReceiver]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html)

## remove_result_receiver

Removes an object which was added as a receiver of captured results.

```python
def remove_result_receiver(self, receiver: CapturedResultReceiver) -> Tuple[int, str]:
```

**Parameters**

`receiver` Specifies a receiver object of the type [`CapturedResultReceiver`]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) to be removed.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html?lang=python)

[CapturedResultReceiver]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html)

## add_result_filter

Adds an object as the filter of captured results.

```python
def add_result_filter(self, filter: CapturedResultFilter) -> Tuple[int, str]:
```

**Parameters**

`filter` Specifies a filter object of the type [`CapturedResultFilter`]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html) to be added.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html?lang=python)

[CapturedResultFilter]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html)

## remove_result_filter

Removes an object which was added as a filter of captured results.

```python
def remove_result_filter(self, filter: CapturedResultFilter) -> Tuple[int, str]:
```

**Parameters**

`filter` Specifies a filter object of the type [`CapturedResultFilter`]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html) to be removed.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html?lang=python)

[CapturedResultFilter]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html)

## start_capturing

Starts to process images consecutively.

```python
def start_capturing(self, template_name: str = "", wait_for_thread_exit: bool = False) -> Tuple[int, str]:
```

**Parameters**

`template_name` Specifies a `CaptureVisionTemplate` to use for capturing.

`wait_for_thread_exit` Indicates whether to wait for the capture process to complete before returning.

**Remarks**

- There are two types of `CaptureVisionTemplate`: the [preset ones]({{ site.dcvb_python_api }}capture-vision-router/enum-preset-template.html) which come with the SDK and the custom ones that get initialized when the user calls [InitSettings]({{ site.dcvb_python_api }}capture-vision-router/settings.html#initsettings) / [InitSettingsFromFile]({{ site.dcvb_python_api }}capture-vision-router/settings.html#initsettingsfromfile).
- Please be aware that the preset `CaptureVisionTemplates` will be overwritten should the user call `InitSettings` / `InitSettingsFromFile` and pass his own settings.
- If parameter `template_name` is not specified, the preset one named 'Default' will be used. However, if the preset ones have been overwritten as described above, the first `CaptureVisionTemplate` from the user's own settings will be used instead.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html?lang=python)

## stop_capturing

Stops the multiple-file processing.

```python
def stop_capturing(self, wait_for_remaining_tasks: bool = True, wait_for_thread_exit: bool = True) -> None:
```

**Parameters**

`wait_for_remaining_tasks` Indicates whether to wait for the remaining tasks to complete before returning. The default value is True.  
`wait_for_thread_exit` Indicates whether to wait for the capture process to complete before returning. The default value is True.


## pause_capturing

Pauses the capture process. The current thread will be blocked until the capture process is resumed.

```python
def pause_capturing(self) -> None:
```

## resume_capturing

Resumes the capture process. The current thread will be unblocked after the capture process is resumed.

```python
def resume_capturing(self) -> None:
```

