---
layout: default-layout
title: class CCaptureStateListener - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the C++ edition of the class CCaptureStateListener in Dynamsoft Capture Vision Router Module.
keywords: capture state listener, c++
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: CVR C++ CCaptureStateListener Class
---

# CCaptureStateListener

The `CCaptureStateListener` class is an abstract class that defines a listener for capture state changes. 

## Definition

*Namespace:* dynamsoft::cvr

*Assembly:* DynamsoftCaptureVisionRouter

```cpp
class CCaptureStateListener
```

## Methods Summary

| Method                                            | Description                            |
| ------------------------------------------------- | -------------------------------------- |
| [`OnCaptureStateChanged`](#oncapturestatechanged) | Called when the capture state changes. |

### OnCaptureStateChanged

Called when the capture state changes.

```cpp
virtual void OnCaptureStateChanged(CaptureState state) = 0;
```

**Parameters**

`[in] state` The new capture state.

**Return value**

This method does not return a value. It is a pure virtual method and must be implemented by a derived class.

**See Also**

[CaptureState]({{ site.dcvb_cpp_api }}capture-vision-router/enum-capture-state.html?src=cpp&&lang=cpp)
