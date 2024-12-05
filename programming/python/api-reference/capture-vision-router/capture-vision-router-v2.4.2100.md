---
layout: default-layout
title: CaptureVisionRouter Class- Dynamsoft Capture Vision Router Module Python Edition API Reference
description: This page is about the CaptureVisionRouter Class of Dynamsoft Capture Vision Router Module Python Edition.
keywords: capture vision router, router, python, api reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# CaptureVisionRouter

The `CaptureVisionRouter` class is what a user uses to interact with image-processing and semantic-processing products in their applications. It accepts an image source and returns processing results which may contain [Final results]({{ site.dcvb_architecture }}output.html#final-results?lang=python).

## Definition

*Module:* dynamsoft_capture_vision_router

```python
class CaptureVisionRouter
```

## Constructor Methods

| Method | Description |
| ------ | ----------- |
| [`__init__`](#__init__) | Initializes a new instance of the `CaptureVisionRouter` class. |

## Single-File Processing Methods

| Method                                         | Description                                               |
| ---------------------------------------------- | --------------------------------------------------------- |
| [`capture`](single-file-processing.md#capture) | Processes an image or file to derive important information. |

## Multiple-File Processing Methods

| Method | Description |
| ------- | ---------- |
| [`set_input`](multiple-file-processing.md#set_input)                                             | Sets an image source to provide images for consecutive process.              |
| [`get_input`](multiple-file-processing.md#get_input)                                             | Gets the attached image source adapter object of the capture vision router.  |
| [`add_capture_state_listener`](multiple-file-processing.md#add_capture_state_listener)               | Adds an object that listens to the state changes of the capture process.     |
| [`remove_capture_state_listener`](multiple-file-processing.md#remove_capture_state_listener)         | Removes an object which listens to the state changes of the capture process. |
| [`add_image_source_state_listener`](multiple-file-processing.md#add_image_source_state_listener)       | Adds an object that listens to state changes of the image source.            |
| [`remove_image_source_state_listener`](multiple-file-processing.md#remove_image_source_state_listener) | Removes an object which listens to state changes of the image source.        |
| [`add_result_receiver`](multiple-file-processing.md#add_result_receiver)                           | Adds an object as the receiver of captured results.                          |
| [`remove_result_receiver`](multiple-file-processing.md#remove_result_receiver)                     | Removes an object which was added as a receiver of captured results.         |
| [`add_result_filter`](multiple-file-processing.md#add_result_filter)                               | Adds an object as the filter of captured results.                            |
| [`remove_result_filter`](multiple-file-processing.md#remove_result_filter)                         | Removes an object which was added as a filter of captured results.           |
| [`start_capturing`](multiple-file-processing.md#start_capturing)                                 | Starts to process images consecutively.                                      |
| [`stop_capturing`](multiple-file-processing.md#stop_capturing)                                   | Stops the consecutive process.                                               |
| [`pause_capturing`](multiple-file-processing.md#pause_capturing)                                 | Pauses the capture process. The current thread will be blocked until the capture process is resumed. |
| [`resume_capturing`](multiple-file-processing.md#resume_capturing)                               | Resumes the capture process. The current thread will be unblocked after the capture process is resumed. |

## Setting Methods

| Method                                                       | Description                                                                                  |
| ------------------------------------------------------------ | -------------------------------------------------------------------------------------------- |
| [`init_settings`](settings.md#init_settings)                   | Loads and initializes a template from a string.                                              |
| [`init_settings_from_file`](settings.md#init_settings_from_file)   | Loads and initializes a template from a file.                                                |
| [`output_settings`](settings.md#output_settings)               | Exports a specific `CaptureVisionTemplate` to a string.                                      |
| [`output_settings_to_file`](settings.md#output_settings_to_file)   | Exports a specific `CaptureVisionTemplate` to a file.                                        |
| [`get_simplified_settings`](settings.md#get_simplified_settings) | Retrieves a `SimplifiedCaptureVisionSettings` object for a specific `CaptureVisionTemplate`. |
| [`update_settings`](settings.md#update_settings)               | Updates a `CaptureVisionTemplate` with `SimplifiedCaptureVisionSettings` object.             |
| [`reset_settings`](settings.md#reset_settings)                 | Resets all templates to factory settings.                                                    |

## Buffered Items Methods

| Method                                                       | Description                                                                                  |
| ------------------------------------------------------------ | -------------------------------------------------------------------------------------------- |
| [`get_buffered_items_manager`](buffered-items.md#get_buffered_items_manager)                   | Gets a `BufferedItemsManager` object.  |

