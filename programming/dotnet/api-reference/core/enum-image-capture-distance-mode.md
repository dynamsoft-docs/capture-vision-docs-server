---
layout: default-layout
title: ImageCaptureDistanceMode - Dynamsoft Core .NET Enumerations
description: The enumeration ImageCaptureDistanceMode of Dynamsoft Core is used to distinguish the close-up images from the prospect images.
keywords: Image capture distance
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
codeAutoHeight: true
---

# Enumeration ImageCaptureDistanceMode

`ImageCaptureDistanceMode` describes the shooting mode of the image. It is used in the `overlap` mode of `Panorama`.

```csharp
public enum EnumImageCaptureDistanceMode
{
   /** The image is taken by close-up shot camera. */
   ICDM_NEAR,
   /** The image is taken by long shot camera. */
   ICDM_FAR
}
```
