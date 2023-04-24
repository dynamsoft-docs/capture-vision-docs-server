---
layout: default-layout
title: class CLicenseManger - Dynamsoft License Module C++ Edition API Reference
description: This page shows the C++ edition of the class CLicenseManger in Dynamsoft License Module.
keywords: license manager, c++
needAutoGenerateSidebar: true
---

# CLicenseManager

The CLicenseManager class provides a set of APIs to manage SDK licensing.

## Definition

*Namespace:* dynamsoft::license

*Assembly:* DynamsoftLicense.dll

```cpp
class CLicenseManager
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`InitLicense`](#initlicense) | Initializes the license using a license key. |
| [`SetDeviceFriendlyName`](#setdevicefriendlyname) | Sets the friendly name of the device. |
| [`SetMaxConcurrentInstanceCount`](#setmaxconcurrentinstancecount) | Sets the maximum number of allowed instances for the given device and process. |
| [`GetDeviceUUID`](#getdeviceuuid) | Gets the unique identifier of the device. |
| [`SetLicenseCachePath`](#setlicensecachepath) | Sets the directory path for the license cache. |
| [`GetVersion`](#getversion) | Gets the version of the licensing library. |

### InitLicense

Initializes the license using a license key.

```cpp
static int InitLicense(const char* pLicense, char errorMsgBuffer[] = NULL, const int errorMsgBufferLen = 0)
```

**Parameters**

`[in] pLicense` The license key as a string.

`[in, out] errorMsgBuffer` The buffer is allocated by caller and the recommended length is 256. The error message will be copied to the buffer. It can be set to NULL if error messages are not required.

`[in] errorMsgBufferLen` The length of the error message buffer. It is ignored if errorMsgBuffer is set to NULL.

**Return value**

Returns 0 if the license is initialized successfully, a negative value indicating an error otherwise.

**Code Snippet**

```cpp
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
if (errorCode != EC_OK)
    cout << szErrorMsg << endl;
```

### SetDeviceFriendlyName

Sets the friendly name of the device.

```cpp
static int SetDeviceFriendlyName(const char* name)
```

**Parameters**

`[in] name` The friendly name of the device.

**Return value**

Returns 0 if the friendly name is set successfully, a negative value indicating an error otherwise.

### SetMaxConcurrentInstanceCount

Sets the maximum number of allowed instances for the given device and process.

```cpp
static void SetMaxConcurrentInstanceCount(int countForThisDevice, int countForThisProcess = 0)
```

**Parameters**

`[in] countForThisDevice` The maximum number of allowed instances for the device.

`[in] countForThisProcess` The maximum number of allowed instances for the process. It is optional and set to 0 by default.

### GetDeviceUUID

Gets the unique identifier of the device.

```cpp
static int GetDeviceUUID(int uuidGenerationMethod, char uuidBuffer[] , const int uuidBufferLen)
```

**Parameters**

`[in] uuidGenerationMethod` The method to generate the UUID.

`[in, out] uuidBuffer` The buffer to store the UUID.

`[in] uuidBufferLen` The length of the UUID buffer. It is recommended to be greater than 36.

**Return value**

Returns 0 if the UUID is generated successfully, a negative value indicating an error otherwise.

### SetLicenseCachePath

Sets the directory path for the license cache.

```cpp
static int SetLicenseCachePath(const char* directoryPath)
```

**Parameters**

`[in] directoryPath` The directory path for the license cache.

**Return value**

Returns 0 if the directory path is set successfully, a negative value indicating an error otherwise.

### GetVersion

Gets the version of the licensing library.

```cpp
static const char* GetVersion()
```

**Return value**

Returns the version of the licensing library as a string.
