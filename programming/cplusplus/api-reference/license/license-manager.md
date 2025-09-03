---
layout: default-layout
title: class CLicenseManager - Dynamsoft License Module C++ Edition API Reference
description: This page shows the C++ edition of the class CLicenseManager in Dynamsoft License Module.
keywords: license manager, c++
needAutoGenerateSidebar: true
---

# CLicenseManager

The `CLicenseManager` class provides a set of APIs to manage SDK licensing.

## Definition

*Namespace:* dynamsoft::license

*Assembly:* DynamsoftLicense

```cpp
class CLicenseManager 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`InitLicense`](#initlicense) | It is used to initialize the license using a license key. |
| [`SetDeviceFriendlyName`](#setdevicefriendlyname) | It is used to set the friendly name of the device. |
| [`SetMaxConcurrentInstanceCount`](#setmaxconcurrentinstancecount) | It is used to set the maximum number of allowed instances for the given device and process. |
| [`GetDeviceUUID`](#getdeviceuuid) | It is used to get the unique identifier of the device. |
| [`SetLicenseCachePath`](#setlicensecachepath) | It is used to set the directory path for the license cache. |

### InitLicense

It is used to initialize the license using a license key.

```cpp
static int InitLicense(const char* pLicense, char errorMsgBuffer[] = NULL, const int errorMsgBufferLen = 0)
```

**Parameters**

`[in] pLicense` The license key as a string.

`[in, out] errorMsgBuffer` The buffer is allocated by caller and the recommended length is 256. The error message will be copied to the buffer. It can be set to NULL if error messages are not required.

`[in] errorMsgBufferLen` The length of the error message buffer. It is ignored if errorMsgBuffer is set to NULL.

**Return value**

Returns 0 if the license is initialized successfully, a negative value indicating an error otherwise.

### SetDeviceFriendlyName

It is used to set the friendly name of the device.

```cpp
static int SetDeviceFriendlyName(const char* name)
```

**Parameters**

`[in] name` The friendly name of the device. If the length exceeds 255, it will be truncated.

**Return value**

Returns 0 if the friendly name is set successfully, a negative value indicating an error otherwise.

**Remarks**

This function must be called before function `InitLicense` to ensure correct functionality.

### SetMaxConcurrentInstanceCount

It is used to set the maximum number of allowed instances for the given device.

```cpp
static int SetMaxConcurrentInstanceCount(int countForThisDevice)
```

**Parameters**

`[in] countForThisDevice` The maximum number of allowed instances for the device.

**Return value**

Returns error code (returns 0 if the function operates successfully). 

**Remarks**

This function must be called before function `InitLicense` to ensure correct functionality.

### GetDeviceUUID

It is used to get the unique identifier of the device.

```cpp
static int GetDeviceUUID(int uuidGenerationMethod, char uuidBuffer[] , const int uuidBufferLen)
```

**Parameters**

`[in] uuidGenerationMethod` The method to generate the UUID.

- 1: Generates UUID with random values.
- 2: Generates UUID based on hardware info.

`[in, out] uuidBuffer` The buffer to store the UUID.

`[in] uuidBufferLen` The length of the UUID buffer. It is recommended to be greater than 36.

**Return value**

Returns 0 if the UUID is generated successfully, a negative value indicating an error otherwise.

**Remarks**

This function must be called before function `InitLicense` to ensure correct functionality.

### SetLicenseCachePath

It is used to set the directory path for the license cache.

```cpp
static int SetLicenseCachePath(const char* directoryPath)
```

**Parameters**

`[in] directoryPath` The directory path for the license cache.

**Return value**

Returns 0 if the directory path is set successfully, a negative value indicating an error otherwise.

**Remarks**

This function must be called before function `InitLicense` to ensure correct functionality.

## Code Snippet

```cpp
int errorCode = 0;
char szErrorMsg[256];
char szUUID[256];
CLicenseManager::SetLicenseCachePath("DIRECTORY-PATH-FOR-LICENSE-CACHE");
CLicenseManager::GetDeviceUUID(1, szUUID, 256);
CLicenseManager::SetDeviceFriendlyName("FRIENDLY-NAME");
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
if (errorCode != ErrorCode::EC_OK && errorCode != ErrorCode::EC_LICENSE_CACHE_USED)
{
    cout << "License initialization failed: ErrorCode: " << errorCode << ", ErrorString: " << szErrorMsg << endl;
}
else
{
    // other codes...
}
```
