---
layout: default-layout
title: class IdentityUtilityModule - Dynamsoft Identity Utility Module Python Edition API Reference
description: API reference for the IdentityUtilityModule class in Dynamsoft Identity Utility Module Python Edition, which provides general functions for the Identity Utility module.
keywords: identity utility module, python
---

# IdentityUtilityModule

The `IdentityUtilityModule` class provides common functions of the identity utility module.

**Remarks**

Introduced in Dynamsoft Capture Vision version 3.4.1000.

## Definition

*Module:* id_utility

```python
class IdentityUtilityModule()
```

## Methods

| Method                                                    | Description                                        |
| --------------------------------------------------------- | -------------------------------------------------- |
| [`get_version`](#get_version)                             | Returns the version of the identity utility module. |

### get_version

Returns the version of the identity utility module.

```python
@staticmethod
def get_version() -> str:
```

**Return value**

Returns a string representing the version of the identity utility module.
