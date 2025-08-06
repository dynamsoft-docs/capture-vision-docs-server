---
layout: default-layout
title: ImageFileFormat - Dynamsoft Core Java Enumerations
description: The enumeration ImageFileFormat of Dynamsoft Core describes the format of image files.
keywords: Image file format
codeAutoHeight: true
---

# Enumeration ImageFileFormat

`ImageFileFormat` categorizes the possible formats of image files.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumImageFileFormat {
    //JPEG image format.
    int IFF_JPEG = 0;
    //PNG image format.
    int IFF_PNG = 1;
    //BMP (Bitmap) image format.
    int IFF_BMP = 2;
    //PDF (Portable Document Format) format.
    int IFF_PDF = 3;
}
```