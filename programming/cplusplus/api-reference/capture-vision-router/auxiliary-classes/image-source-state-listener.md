---
layout: default-layout
title: class CImageSourceStateListener - Dynamsoft Capture Vision Router Module C++ Edition API Reference
description: This page shows the C++ edition of the class CImageSourceStateListener in Dynamsoft Capture Vision Router Module.
keywords: image source state listener, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: CVR C++ CImageSourceStateListener Class
---

# CImageSourceStateListener

The `CImageSourceStateListener` class is an abstract class that defines a listener for image source state changes.

## Definition

*Namespace:* dynamsoft::cvr

*Assembly:* DynamsoftCaptureVisionRouter

```cpp
class CImageSourceStateListener 
```

## Methods

| Method                                                    | Description                                        |
| --------------------------------------------------------- | -------------------------------------------------- |
| [`OnImageSourceStateReceived`](#onimagesourcestatereceived) | Called when the state of the image source changes. |

### OnImageSourceStateReceived

This method is called when the state of the image source changes.

```cpp
virtual void OnImageSourceStateReceived(ImageSourceState state) = 0;
```

**Parameters**

`[in] state` The state of the image source.

**Return value**

This method does not return a value. It is a pure virtual function that must be implemented by any class that derives from CImageSourceStateListener.

**See Also**

[ImageSourceState]({{ site.dcvb_cpp_api }}capture-vision-router/enum-image-source-state.html?src=cpp&&lang=cpp)
