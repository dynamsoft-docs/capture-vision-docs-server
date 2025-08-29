---
layout: default-layout
title: CaptureVisionError Class - Dynamsoft Capture Vision Router Module Java Edition API Reference
description: Definition of CaptureVisionError class in Dynamsoft Capture Vision Router Module Java Edition.
keywords: capture vision router module, java
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# CaptureVisionError

The `CaptureVisionError` class represents an error object that contains error code and error string information. This class extends [`CoreError`]({{ site.dcvb_java_api }}core/core-error.html) and provides specific error handling for capture vision router operations.

## Definition

*Package:* com.dynamsoft.cvr

```java
public class CaptureVisionError extends CoreError
```

## Inheritance

`CaptureVisionError` -> [`CoreError`]({{ site.dcvb_java_api }}core/core-error.html)

## Inherited Members

Since `CaptureVisionError` extends [`CoreError`]({{ site.dcvb_java_api }}core/core-error.html), it inherits all the properties and methods from the parent class, including:

- `getErrorCode()` - Returns the error code.
- `getErrorString()` - Returns the error string.

