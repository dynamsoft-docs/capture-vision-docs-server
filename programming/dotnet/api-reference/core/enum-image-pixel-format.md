---
layout: default-layout
title: ImagePixelFormat - Dynamsoft Core .NET Enumerations
description: The enumeration ImagePixelFormat describes all supported image pixel formats for .NET Edition.
keywords: Image pixel format
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
codeAutoHeight: true
---

# Enumeration ImagePixelFormat

`ImagePixelFormat` defines the range of pixel formats that an image can have, specifying how color and transparency data are represented in each pixel of the image.

```csharp
public enum EnumImagePixelFormat
{
   /** 0:Black, 1:White. */
   IPF_BINARY,
   /** 0:White, 1:Black. */
   IPF_BINARYINVERTED,
   /** 8bit gray. */
   IPF_GRAYSCALED,
   /** NV21. */
   IPF_NV21,
   /** 16bit with RGB channel order stored in memory from high to low address. */
   IPF_RGB_565,
   /** 16bit with RGB channel order stored in memory from high to low address. */
   IPF_RGB_555,
   /** 24bit with RGB channel order stored in memory from high to low address. */
   IPF_RGB_888,
   /** 32bit with ARGB channel order stored in memory from high to low address. */
   IPF_ARGB_8888,
   /** 48bit with RGB channel order stored in memory from high to low address. */
   IPF_RGB_161616,
   /** 64bit with ARGB channel order stored in memory from high to low address. */
   IPF_ARGB_16161616,
   /** 32bit with ABGR channel order stored in memory from high to low address. */
   IPF_ABGR_8888,
   /** 64bit with ABGR channel order stored in memory from high to low address. */
   IPF_ABGR_16161616,
   /** 24bit with BGR channel order stored in memory from high to low address. */
   IPF_BGR_888,
   /** 8-bit binary. 0:Black, 255:White. Foreground (bars) are black, background (spaces) are white. */
   IPF_BINARY_8,
   /**NV12 */
   IPF_NV12,
   /**8-bit binary. 0:Black, 255:White. Foreground (bars) are white, background (spaces) are black. */
   IPF_BINARY_8_INVERTED
}
```