---
layout: default-layout
title: LicenseManager Class - Dynamsoft License Module .NET Edition API Reference
description: Definition of LicenseManager class in Dynamsoft License Module .NET Edition.
keywords: license manager, .NET
needAutoGenerateSidebar: true
---

# LicenseManager

The `LicenseManager` class provides a set of APIs to manage SDK licensing.

## Definition

*Namespace:* Dynamsoft.License


```csharp
public static class LicenseManager 
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`InitLicense`](#initlicense) | Initializes the license using a license key. |
| [`SetDeviceFriendlyName`](#setdevicefriendlyname) | Sets the friendly name of the device. |
| [`SetMaxConcurrentInstanceCount`](#setmaxconcurrentinstancecount) | Sets the maximum number of allowed instances for the given device and process. |
| [`GetDeviceUUID`](#getdeviceuuid) | Gets the unique identifier of the device. |
| [`SetLicenseCachePath`](#setlicensecachepath) | Sets the directory path for the license cache. |

### InitLicense

Initializes the license using a license key.

```csharp
static int InitLicense(string license, out string errorMsg)
```

**Parameters**

`[in] license` The license key as a string.

`[out] errorMsg` The detailed error message.

**Return Value**

Returns 0 if the license is initialized successfully, a negative value indicating an error otherwise.

**See Also**

[EnumErrorCode]({{ site.dcvb_dotnet_api }}core/enum-error-code.html)

### SetDeviceFriendlyName

Sets the friendly name of the device.

```csharp
static int SetDeviceFriendlyName(string name)
```

**Parameters**

`[in] name` The friendly name of the device.

**Return Value**

Returns 0 if the friendly name is set successfully, a negative value indicating an error otherwise.

**Remarks**

This function must be called before function `InitLicense` to ensure correct functionality.

**See Also**

[EnumErrorCode]({{ site.dcvb_dotnet_api }}core/enum-error-code.html)

### SetMaxConcurrentInstanceCount

Sets the maximum number of allowed instances for the given device.

```csharp
static int SetMaxConcurrentInstanceCount(int countForThisDevice)
```

**Parameters**

`[in] countForThisDevice` The maximum number of allowed instances for the device.

**Return Value**

Returns error code (returns 0 if the function operates successfully). 

**Remarks**

This function must be called before function `InitLicense` to ensure correct functionality.

**See Also**

[EnumErrorCode]({{ site.dcvb_dotnet_api }}core/enum-error-code.html)

### GetDeviceUUID

Gets the unique identifier of the device.

```csharp
static int GetDeviceUUID(int uuidGenerationMethod, out string uuid)
```

**Parameters**

`[in] uuidGenerationMethod` The method to generate the UUID.

- 1: Generates UUID with random values.
- 2: Generates UUID based on hardware info.

`[out] uuid` The unique identifier of the device.

**Return Value**

Returns 0 if the UUID is generated successfully, a negative value indicating an error otherwise.

**Remarks**

This function must be called before function `InitLicense` to ensure correct functionality.

### SetLicenseCachePath

Sets the directory path for the license cache.

```csharp
static int SetLicenseCachePath(string directoryPath)
```

**Parameters**

`[in] directoryPath` The directory path for the license cache.

**Return Value**

Returns 0 if the directory path is set successfully, a negative value indicating an error otherwise.

**Remarks**

This function must be called before function `InitLicense` to ensure correct functionality.

**See Also**

[EnumErrorCode]({{ site.dcvb_dotnet_api }}core/enum-error-code.html)

## Code Snippet

```csharp
int errorCode = 0;
string deviceUUID;
string errorMsg;
LicenseManager.SetLicenseCachePath("DIRECTORY-PATH-FOR-LICENSE-CACHE");
LicenseManager.GetDeviceUUID(1, out deviceUUID);
LicenseManager.SetDeviceFriendlyName("FRIENDLY-NAME");
errorCode = LicenseManager.InitLicense("YOUR-LICENSE-KEY", out errorMsg);
if (errorCode != (int)EnumErrorCode.EC_OK && errorCode != (int)EnumErrorCode.EC_LICENSE_CACHE_USED)
{
    Console.WriteLine("License initialization error: " + errorMsg);
}
else
{
    CaptureVisionRouter cvr = new CaptureVisionRouter();
    // add code for further process
}
```
