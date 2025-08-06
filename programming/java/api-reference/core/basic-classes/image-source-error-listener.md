---
layout: default-layout
title: ImageSourceErrorListener Class - Dynamsoft Capture Vision Module Java Edition API Reference
description: Definition of ImageSourceErrorListener class in Dynamsoft Core Module Java Edition.
keywords: imagesource error listener, java
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# ImageSourceErrorListener

The `ImageSourceErrorListener` interface defines a listener for receiving error notifications from an image source.

## Definition

*Package:* `com.dynamsoft.core.basic_structures`

```java
public interface ImageSourceErrorListener
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`onErrorReceived`](#onerrorreceived) | Called when an error is received from the image source. |

### onErrorReceived

Called when an error is received from the image source.

```java
void onErrorReceived(int errorCode, String errorMessage)
```

**Parameters**

`errorCode` The integer error code indicating the type of error.

`errorMessage` A string containing the error message providing additional information about the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_java_api }}core/enum-error-code.html)
