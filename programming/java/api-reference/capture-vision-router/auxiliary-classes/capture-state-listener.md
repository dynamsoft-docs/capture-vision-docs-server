---
layout: default-layout
title: CaptureStateListener Interface - Dynamsoft Capture Vision Module Java Edition API Reference
description: Definition of CaptureStateListener interface in Dynamsoft Capture Vision Module Java Edition.
keywords: capture state listener, java
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# CaptureStateListener

Defines a listener for capture state changes.

## Definition

*Namespace:* com.dynamsoft.cvr

```java
interface CaptureStateListener
```

## Methods

| Method                                            | Description                            |
| ------------------------------------------------- | -------------------------------------- |
| [`onCaptureStateChanged`](#oncapturestatechanged) | Called when the capture state changes. |

### onCaptureStateChanged

Called when the capture state changes.

```java
default void onCaptureStateChanged(@EnumCaptureState int state)
```

**Parameters**

`state` The new capture state. It is one of the values of the `EnumCaptureState` enumeration.

**See Also**

[EnumCaptureState]({{ site.dcvb_java_api }}capture-vision-router/enum-capture-state.html)
