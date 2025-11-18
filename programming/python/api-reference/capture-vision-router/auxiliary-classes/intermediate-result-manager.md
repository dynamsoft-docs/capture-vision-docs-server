---
layout: default-layout
title: class IntermediateResultManager - Dynamsoft Capture Vision Router Python Edition API Reference
description: This page shows the Python Edition of the class IntermediateResultManager in Dynamsoft Capture Vision Router Module.
keywords: intermediate result manager, python
needAutoGenerateSidebar: true
---

# IntermediateResultManager

The `IntermediateResultManager` class manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get original image data using an image hash id.

## Definition

*Module:* dynamsoft_capture_vision_router

```python
class IntermediateResultManager 
```

## Methods

| Method | Description |
|--------|-------------|
| [`add_result_receiver`](#add_result_receiver) | Adds an intermediate result receiver.|
| [`remove_result_receiver`](#remove_result_receiver) | Removes an intermediate result receiver. |
| [`get_original_image`](#get_original_image) | Gets the original image data using an image hash id. |

### add_result_receiver

Adds an intermediate result receiver to the manager.

```python
def add_result_receiver(self, receiver: IntermediateResultReceiver) -> int:
```

**Parameters**

`receiver` The intermediate result receiver to add.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[IntermediateResultReceiver]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/intermediate-result-receiver.html)

### remove_result_receiver

Removes an intermediate result receiver from the manager.

```python
def remove_result_receiver(self, receiver: IntermediateResultReceiver) -> int:
```

**Parameters**

`receiver` The intermediate result receiver to remove.

**Return value**

Returns 0 if succeeds, nonzero otherwise.

**See Also**

[IntermediateResultReceiver]({{ site.dcvb_python_api }}capture-vision-router/auxiliary-classes/intermediate-result-receiver.html)

### get_original_image

Gets the original image data using an image hash id.

```python
def get_original_image(self, image_hash_id: str)->ImageData:
```

**Parameters**

`image_hash_id` The hash id of the image to retrieve.

**Return value**

Returns an `ImageData` object containing the original image data.

**See Also**

[ImageData]({{ site.dcvb_python_api }}core/basic-classes/image-data.html)
