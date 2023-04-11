---
layout: default-layout
title: class CLicenseManger - Dynamsoft License Module C++ Edition API Reference
description: This page shows the C++ edition of the class CLicenseManger in Dynamsoft License Module.
keywords: license manager, c++
needAutoGenerateSidebar: true
---

# CLicenseManager

[Given a short description about the class]

```cpp
class dynamsoft::license::CLicenseManager 
```

| Method | Description |
|--------|-------------|
| [`InitLicense`](#initlicense) | Sets the license key and activates the SDK.|

## InitLicense

Sets the license key and activates the SDK.

```cpp
static int InitLicense(const char *license, char errorMsgBuffer[], const int errorMsgBufferLen) 
```

**Parameters**

`[in] pLicense` The license key.

`[in, out] errorMsgBuffer` The buffer is allocated by caller and the recommended length is 256. The error message will be copied to the buffer.

`[in] errorMsgBufferLen` The length of the allocated buffer.

**Return Value**

Returns error code (returns 0 if the function operates successfully).

**Code Snippet**

```cpp
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("YOUR-LICENSE-KEY", szErrorMsg, 256);
if (errorCode != EC_OK)
    cout << szErrorMsg << endl;
```
