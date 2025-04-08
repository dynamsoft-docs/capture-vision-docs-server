---
layout: default-layout
title: ImageSourceErrorListener Class - Dynamsoft Capture Vision Module Python Edition API Reference
description: Definition of ImageSourceErrorListener class in Dynamsoft Core Module Python Edition.
keywords: imagesource error listener, python
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# ImageSourceErrorListener

The `ImageSourceErrorListener` class defines a listener for receiving error notifications from an image source.

>Note: Subclasses inheriting from this class must ensure that the parent class constructor (`super().__init__()`) is properly called to guarantee correct initialization.

## Definition

*Module:* dynamsoft_core

```python
class ImageSourceErrorListener(ABC) 
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`on_error_received`](#on_error_received) | Called when an error is received from the image source. |

### on_error_received

Called when an error is received from the image source.

```python
@abstractmethod
def on_error_received(self, error_code: int, error_message: str) -> None:
```

**Parameters**

`error_code` The integer error code indicating the type of error.

`error_message` A string containing the error message providing additional information about the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_python_api }}core/enum-error-code.html?lang=python)
