---
layout: default-layout
title: CaptureVisionRouter Auxiliary Methods - Dynamsoft Capture Vision Python Edition API
description: This page introduces auxiliary methods of the CaptureVisionRouter class of the Dynamsoft Capture Vision Python Edition.
keywords: capture vision, auxiliary, instance, api reference, Python
needAutoGenerateSidebar: true
needGenerateH3Content: false
---

# Auxiliary Methods - CaptureVisionRouter Class

| Method                                                      | Description                                               |
| ----------------------------------------------------------- | --------------------------------------------------------- |
| [`set_global_intra_op_num_threads`](#set_global_intra_op_num_threads) | Sets the global number of threads used internally for model execution. |
| [`append_dl_model_buffer`](#append_dl_model_buffer) | Appends a deep learning model to the memory buffer. |
| [`clear_dl_model_buffers`](#clear_dl_model_buffers) | Clears all deep learning models from buffer to free up memory. |
| [`append_model_buffer`](#append_model_buffer) | Deprecated. Will be removed in future versions. Use `append_dl_model_buffer` instead. |

## set_global_intra_op_num_threads

Sets the global number of threads used internally for model execution.

```python
@staticmethod
def set_global_intra_op_num_threads(intra_op_num_threads: int) -> None
```

**Parameters**

`intra_op_num_threads` (*int*): Number of threads used internally for model execution. Valid range: [0, 256]. 
If the value is outside the range [0, 256], it will be treated as 0 (default).

**Remarks**

- Introduced in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.

## append_dl_model_buffer

Appends a deep learning model to the memory buffer.

```python
@staticmethod
def append_dl_model_buffer(model_name: str, model_buffer: bytes, max_model_instances: int) -> Tuple[int, str]
```

**Parameters**

`model_name` (*str*): The name of the model.

`model_buffer` (*bytes*): The bytes of the model.

`max_model_instances` (*int*): The max instances created for the model.

**Return Value**

A tuple containing following elements:
- `error_code` (*int*): The error code indicating the status of the operation.
- `error_message` (*str*): A descriptive message explaining the error.

**Remarks**

- Introduced in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.

## clear_dl_model_buffers

Clears all deep learning models from buffer to free up memory.

```python
@staticmethod
def clear_dl_model_buffers() -> None
```

**Remarks**

- After calling this function, all `CaptureVisionRouter` instances created before the function call will not be able to use model-related features.

- Introduced in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.

## append_model_buffer

Deprecated. Will be removed in future versions. Use `append_dl_model_buffer` instead.

**Remarks**

- Deprecated in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.
