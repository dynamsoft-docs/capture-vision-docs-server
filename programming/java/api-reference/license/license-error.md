---
layout: default-layout
title: LicenseError Class - Dynamsoft License Module Java Edition API Reference
description: Definition of LicenseError class in Dynamsoft License Module Java Edition.
keywords: license module, java
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# LicenseError

The `LicenseError` class represents an error object that contains error code and error string information. This class extends [`CoreError`]({{ site.dcvb_java_api }}core/core-error.html) and provides specific error handling for license operations.

## Definition

*Package:* com.dynamsoft.license

```java
public class LicenseError extends CoreError
```

## Inheritance

`LicenseError` -> [`CoreError`]({{ site.dcvb_java_api }}core/core-error.html)

## Inherited Members

Since `LicenseError` extends [`CoreError`]({{ site.dcvb_java_api }}core/core-error.html), it inherits all the properties and methods from the parent class, including:

- `getErrorCode()` - Returns the error code.
- `getErrorString()` - Returns the error string.

