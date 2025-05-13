---
layout: default-layout
title: BufferOverflowProtectionMode - Dynamsoft Core .NET Enumerations
description: The enumeration BufferOverflowProtectionMode describes the protection modes when the buffer of ImageSourceAdapter is overflow for .NET Edition.
keywords: Buffer overflow protection mode 
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
codeAutoHeight: true
---

# Enumeration BufferOverflowProtectionMode

`BufferOverflowProtectionMode` describes the protection modes to manage situations when the `ImageSourceAdapter`'s buffer exceeds its capacity. 

```csharp
public enum EnumBufferOverflowProtectionMode
{
   /** New images are blocked when the buffer is full. */
   BOPM_BLOCK = 0,
   /** New images are appended at the end, and oldest images are pushed out from the beginning if the buffer is full. */
   BOPM_UPDATE = 1
}
```