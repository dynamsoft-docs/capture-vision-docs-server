---
layout: default-layout
title: LicenseManager Class - Dynamsoft License Module Java Edition API Reference
description: Definition of LicenseManager class in Dynamsoft License Module Java Edition.
keywords: license manager, java
needAutoGenerateSidebar: true
---

# LicenseManager

The `LicenseManager` class provides a set of APIs to manage SDK licensing.

## Definition

*Namespace:* com.dynamsoft.license

```java
public class LicenseManager
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`initLicense`](#initlicense) | Initializes the license using a license key. |
| [`setDeviceFriendlyName`](#setdevicefriendlyname) | Sets the friendly name of the device. |
| [`setMaxConcurrentInstanceCount`](#setmaxconcurrentinstancecount) | Sets the maximum number of allowed instances for the given device and process. |
| [`getDeviceUUID`](#getdeviceuuid) | Gets the unique identifier of the device. |
| [`setLicenseCachePath`](#setlicensecachepath) | Sets the directory path for the license cache. |

### initLicense

Initializes the license using a license key.

```java
static LicenseError initLicense(String license) throws LicenseException
```

**Parameters**

`license` The license key as a string.

**Return Value**

Returns a `LicenseError` object containing error information.

**Exception**

[`LicenseException`](license-exception.html)

**See Also**

[EnumErrorCode]({{ site.dcvb_java_api }}core/enum-error-code.html)

### setDeviceFriendlyName

Sets the friendly name of the device.

```java
static void setDeviceFriendlyName(String name) throws LicenseException
```

**Parameters**

`name` The friendly name of the device.

**Exception**

[`LicenseException`](license-exception.html)

**Remarks**

This function must be called before function `initLicense` to ensure correct functionality.

**See Also**

[EnumErrorCode]({{ site.dcvb_java_api }}core/enum-error-code.html)

### setMaxConcurrentInstanceCount

Sets the maximum number of allowed instances for the given device.

```java
static void setMaxConcurrentInstanceCount(int countForThisDevice) throws LicenseException
```

**Parameters**

`countForThisDevice` The maximum number of allowed instances for the device.

**Exception**

[`LicenseException`](license-exception.html)

**Remarks**

This function must be called before function `initLicense` to ensure correct functionality.

**See Also**

[EnumErrorCode]({{ site.dcvb_java_api }}core/enum-error-code.html)

### getDeviceUUID

Gets the unique identifier of the device.

```java
static char[] getDeviceUUID(int uuidGenerationMethod) throws LicenseException
```

**Parameters**

`uuidGenerationMethod` The method to generate the UUID.

- 1: Generates UUID with random values.
- 2: Generates UUID based on hardware info.

**Return Value**

Returns a char array representing the unique identifier of the device.

**Exception**

[`LicenseException`](license-exception.html)

**Remarks**

This function must be called before function `initLicense` to ensure correct functionality.

### setLicenseCachePath

Sets the directory path for the license cache.

```java
static void setLicenseCachePath(String directoryPath) throws LicenseException
```

**Parameters**

`directoryPath` The directory path for the license cache.

**Exception**

[`LicenseException`](license-exception.html)

**Remarks**

This function must be called before function `initLicense` to ensure correct functionality.

**See Also**

[EnumErrorCode]({{ site.dcvb_java_api }}core/enum-error-code.html)

## Code Snippet

```java
try {
    LicenseManager.setLicenseCachePath("DIRECTORY-PATH-FOR-LICENSE-CACHE");
    char[] deviceUUID = LicenseManager.getDeviceUUID(1);
    LicenseManager.setDeviceFriendlyName("FRIENDLY-NAME");
    LicenseError licenseError = LicenseManager.initLicense("YOUR-LICENSE-KEY");
    if (licenseError.getErrorCode() != EnumErrorCode.EC_OK && 
        licenseError.getErrorCode() != EnumErrorCode.EC_LICENSE_CACHE_USED) {
        System.out.println("License initialization error: " + licenseError.getErrorString());
    } else {
        CaptureVisionRouter cvrInstance = new CaptureVisionRouter();
        // add code for further process
    }
} catch (LicenseException e) {
    e.printStackTrace();
}
```
