---
layout: default-layout
title: class CCoreModule - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the C++ edition of the class CCoreModule in Dynamsoft Utility Module.
keywords: core module, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: C++ CCoreModule Class
---

# CCoreModule

The `CCoreModule` class defines general functions in the core module.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore

```cpp
class CCoreModule 
```

## Methods Summary

| Method                                                    | Description                                        |
| --------------------------------------------------------- | -------------------------------------------------- |
| [GetVersion](#getversion)                                     | Returns the version of the core module. |
| [AllocateBytes](#allocatebytes)                                     | Allocates a block of memory. |
| [FreeBytes](#freebytes)                                     | Frees a block of memory. |

## GetVersion

Returns the version of the core module.

```cpp
static const char* GetVersion();
```

**Parameters**

None.

**Return Value**

Returns a const char pointer representing the version of the core module.

## AllocateBytes

Allocates a block of memory.

```cpp
static void* AllocateBytes(size_t length);
```

**Parameters**

`[in] length` The number of bytes to allocate.

**Return Value**

Returns a pointer to the allocated memory.

## FreeBytes

Frees a block of memory.

```cpp
static void FreeBytes(void* ptr);
```

**Parameters**

`[in] ptr` A pointer to the memory to free.

