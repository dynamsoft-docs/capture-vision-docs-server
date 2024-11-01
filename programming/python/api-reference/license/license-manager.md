---
layout: default-layout
title: LicenseManager Class - Dynamsoft License Module Python Edition API Reference
description: Definition of LicenseManager class in Dynamsoft License Module Python Edition.
keywords: license manager, python
needAutoGenerateSidebar: true
---

# LicenseManager

The `LicenseManager` class provides a set of APIs to manage SDK licensing.

## Definition

*Module:* dynamsoft_license

```python
class LicenseManager(object)
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`init_license`](#init_license) | Initializes the license using a license key. |
| [`set_device_friendly_name`](#set_device_friendly_name) | Sets the friendly name of the device. |
| [`set_max_concurrent_instance_count`](#set_max_concurrent_instance_count) | Sets the maximum number of allowed instances for the given device and process. |
| [`get_device_uuid`](#get_device_uuid) | Gets the unique identifier of the device. |
| [`set_license_cache_path`](#set_license_cache_path) | Sets the directory path for the license cache. |

### init_license

Initializes the license using a license key.

```python
@staticmethod
def init_license(license: str) -> Tuple[int, str]:
```

**Parameters**

`license` The license key as a string.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_enumerations }}core/error-code.html?lang=python)

### set_device_friendly_name

Sets the friendly name of the device.

```python
@staticmethod
def set_device_friendly_name(name: str) -> Tuple[int, str]:
```

**Parameters**

`name` The friendly name of the device.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**Remarks**

This function must be called before function `init_license` to ensure correct functionality.

**See Also**

[EnumErrorCode]({{ site.dcvb_enumerations }}core/error-code.html?lang=python)

### set_max_concurrent_instance_count

Sets the maximum number of allowed instances for the given device.

```python
@staticmethod
def set_max_concurrent_instance_count(count_for_this_device: int) -> Tuple[int, str]:
```

**Parameters**

`count_for_this_device` The maximum number of allowed instances for the device.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**Remarks**

This function must be called before function `init_license` to ensure correct functionality.

**See Also**

[EnumErrorCode]({{ site.dcvb_enumerations }}core/error-code.html?lang=python)

### get_device_uuid

Gets the unique identifier of the device.

```python
@staticmethod
def get_device_uuid(uuid_generation_method: int) -> Tuple[int, str, str]:
```

**Parameters**

`uuid_generation_method` The method to generate the UUID.

- 1: Generates UUID with random values.
- 2: Generates UUID based on hardware info.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.
- `uuid` <*str*>: The unique identifier of the device.

**Remarks**

This function must be called before function `init_license` to ensure correct functionality.

### set_license_cache_path

Sets the directory path for the license cache.

```python
@staticmethod
def set_license_cache_path(directory_path: str) -> Tuple[int, str]:
```

**Parameters**

`directory_path` The directory path for the license cache.

**Return Value**

Returns a tuple containing following elements:
- `error_code` <*int*>: The error code indicating the status of the operation.
- `error_message` <*str*>: A descriptive message explaining the error.

**Remarks**

This function must be called before function `init_license` to ensure correct functionality.

**See Also**

[EnumErrorCode]({{ site.dcvb_enumerations }}core/error-code.html?lang=python)

## Code Snippet

```python
error_code = 0
LicenseManager.set_license_cache_path("DIRECTORY-PATH-FOR-LICENSE-CACHE")
device_uuid = LicenseManager.get_device_uuid(1)
LicenseManager.set_device_friendly_name("FRIENDLY-NAME")
error_code, error_msg = LicenseManager.init_license("YOUR-LICENSE-KEY")
if error_code != EnumErrorCode.EC_OK.value and error_code != EnumErrorCode.EC_LICENSE_CACHE_USED.value:
    print("License initialization error: " + error_msg)
else:
    CaptureVisionRouter cvr = new CaptureVisionRouter()
    # add code for further process
```
