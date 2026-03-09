---
layout: default-layout
title: class CIdentityUtilityModule - Dynamsoft Identity Utility Module C++ Edition API Reference
description: API reference for the CIdentityUtilityModule class in Dynamsoft Identity Utility C++ Edition, providing module-level utilities such as version retrieval.
keywords: identity utility module, c++
---

# CIdentityUtilityModule

The `CIdentityUtilityModule` class provides common functions of the identity utility module.

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

## Definition

*Namespace:* dynamsoft::id_utility

*Assembly:* DynamsoftIdentityUtility

```cpp
class CIdentityUtilityModule
```

## Methods

| Method                                                    | Description                                        |
| --------------------------------------------------------- | -------------------------------------------------- |
| [GetVersion](#getversion)                                     | Gets the version of the identity utility module. |

### GetVersion

Gets the version of the identity utility module.

```cpp
static const char* GetVersion();
```

**Return Value**

Returns the version string.
