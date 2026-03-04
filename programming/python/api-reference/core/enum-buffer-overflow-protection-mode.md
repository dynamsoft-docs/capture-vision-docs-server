---
layout: default-layout
title: BufferOverflowProtectionMode - Dynamsoft Core Python Enumerations
description: The enumeration BufferOverflowProtectionMode in Dynamsoft Core Python Edition describes the strategy applied when the ImageSourceAdapter image buffer overflows (ignore new or update oldest).
keywords: Buffer overflow protection mode 
codeAutoHeight: true
---

# Enumeration BufferOverflowProtectionMode

`BufferOverflowProtectionMode` describes the protection modes to manage situations when the `ImageSourceAdapter`'s buffer exceeds its capacity. 

```python
class EnumBufferOverflowProtectionMode(IntEnum):
    # New images are blocked when the buffer is full. 
    BOPM_BLOCK = 0x00
    # New images are appended at the end, and the oldest images are pushed out from the beginning if the buffer is full. 
    BOPM_UPDATE = 0x01
```