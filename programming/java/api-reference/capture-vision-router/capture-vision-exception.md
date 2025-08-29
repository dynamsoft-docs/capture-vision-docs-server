---
layout: default-layout
title: CaptureVisionException Class - Dynamsoft Capture Vision Router Module Java Edition API Reference
description: Definition of CaptureVisionException class in Dynamsoft Capture Vision Router Module Java Edition.
keywords: capture vision router module, java
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# CaptureVisionException

The `CaptureVisionException` class is the base exception class used by Dynamsoft Capture Vision Router module. This class extends the standard Java `Exception` class and provides additional error code and error string information for more detailed error handling.

## Definition

*Package:* com.dynamsoft.cvr

```java
public class CaptureVisionException extends Exception
```

## Inheritance

`CaptureVisionException` -> `Exception` -> `Throwable`

## Methods

| Method | Description |
| ------ | ----------- |
| [`getErrorCode()`](#geterrorcode) | Returns the error code associated with the exception. |
| [`getErrorString()`](#geterrorstring) | Returns the error string associated with the exception. |

### getErrorCode()

Returns the error code associated with the exception.

```java
public int getErrorCode()
```

**Return Value**

The error code as an integer value.

**See Also**

[EnumErrorCode]({{ site.dcvb_java_api }}core/enum-error-code.html)

### getErrorString()

Returns the error string associated with the exception.

```java
public String getErrorString()
```

**Return Value**

The error string that provides additional details about the error.

## Inherited Members

Since `CaptureVisionException` extends `Exception`, it also inherits all standard exception methods such as `getMessage()`, `getCause()`, `printStackTrace()`, etc.

