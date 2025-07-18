---
layout: default-layout
title: ColourChannelUsageType - Dynamsoft Core .NET Enumerations
description: The enumeration ColourChannelUsageType describes how the color channel is used in the image for .NET Edition.
keywords: Corner type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
codeAutoHeight: true
---

# Enumeration ColourChannelUsageType

`ColourChannelUsageType` enumerates the different ways color channels can be utilized in image processing. This allows for flexible image analysis and manipulation by specifying how color data should be handled.

```csharp
public enum EnumColourChannelUsageType
{
    /** Automatic color channel usage determination based on image pixel format and scene. */
    CCUT_AUTO,
    /** Use all available color channels for processing. */
    CCUT_FULL_CHANNEL,
    /** Use only the Y (luminance) channel for processing in images represented in the NV21 format. */
    CCUT_NV21_Y_CHANNEL_ONLY,
    /** Use only the red channel for processing in RGB images.*/
    CCUT_RGB_R_CHANNEL_ONLY,
    /** Use only the green channel for processing in RGB images.*/
    CCUT_RGB_G_CHANNEL_ONLY,
    /** Use only the blue channel for processing in RGB images.*/
    CCUT_RGB_B_CHANNEL_ONLY
}
```