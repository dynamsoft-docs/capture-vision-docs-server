---
layout: default-layout
title: class CImageSourceStateListener - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the C++ edition of the class CImageSourceStateListener in Dynamsoft Capture Vision Router Module.
keywords: image source state listener, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: CVR C++ CImageSourceStateListener Class
permalink: /programming/cplusplus/api-reference/capture-vision-router/auxiliary-classes/image-source-state-listener.html
---

# CImageSourceStateListener

The `CImageSourceStateListener` class is an abstract class that defines a listener for image source state changes.

## Definition

*Namespace:* dynamsoft::cvr

*Assembly:* DynamsoftCaptureVisionRouter.dll

```cpp
class CImageSourceStateListener 
```

## Methods Summary

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