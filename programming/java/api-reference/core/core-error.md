---
layout: default-layout
title: CoreError Class - Dynamsoft Core Module Java Edition API Reference
description: Definition of CoreError class in Dynamsoft Core Module Java Edition.
keywords: core module, java
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# CoreError

The `CoreError` class represents an error object that contains error code and error string information. This class is used to provide detailed error information within the Dynamsoft SDK.

## Definition

*Package:* com.dynamsoft.core

```java
public class CoreError
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getErrorCode()`](#geterrorcode) | Returns the error code. |
| [`getErrorString()`](#geterrorstring) | Returns the error string. |

### getErrorCode()

Returns the error code.

```java
public int getErrorCode()
```

**Return Value**

The error code as an integer value.

**See Also**

[EnumErrorCode]({{ site.dcvb_java_api }}core/enum-error-code.html)

### getErrorString()

Returns the error string associated with the error code.

```java
public String getErrorString()
```

**Return Value**

The error string that provides additional details about the error.

