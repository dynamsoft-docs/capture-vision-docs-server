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

```cpp
class dynamsoft::cvr::CImageSourceStateListener 
```

## Methods Summary

| Method                                                    | Description                                        |
| --------------------------------------------------------- | -------------------------------------------------- |
| [`OnImageSourceStateChanged`](#onimagesourcestatechanged) | Called when the state of the image source changes. |

### OnImageSourceStateChanged

This method is called when the state of the image source changes.

```cpp
virtual void OnImageSourceStateChanged(ImageSourceState state) = 0;
```

**Parameters**

`[in] state` The new state of the image source.

**Return value**

This method does not return a value. It is a pure virtual function that must be implemented by any class that derives from CImageSourceStateListener.