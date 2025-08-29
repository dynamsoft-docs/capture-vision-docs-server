---
layout: default-layout
title: CoreException Class - Dynamsoft Core Module Java Edition API Reference
description: Definition of CoreException class in Dynamsoft Core Module Java Edition.
keywords: core module, java
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# CoreException

The `CoreException` class is the base exception class used by Dynamsoft SDK modules. This class extends the standard Java `Exception` class and provides additional error code and error string information for more detailed error handling.

## Definition

*Package:* com.dynamsoft.core

```java
public class CoreException extends Exception
```

## Inheritance

`CoreException` -> `Exception` -> `Throwable`

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

Since `CoreException` extends `Exception`, it also inherits all standard exception methods such as `getMessage()`, `getCause()`, `printStackTrace()`, etc.

