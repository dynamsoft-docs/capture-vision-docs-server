---
layout: default-layout
title: ImageSourceStateListener Interface - Dynamsoft Capture Vision Router Module Java Edition API Reference
description: Definition of ImageSourceStateListener interface in Dynamsoft Capture Vision Module Java Edition.
keywords: image source state listener, java
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# ImageSourceStateListener

Defines a listener for image source state changes.

## Definition

*Namespace:* com.dynamsoft.cvr

```java
interface ImageSourceStateListener
```

## Methods

| Method                                                    | Description                                        |
| --------------------------------------------------------- | -------------------------------------------------- |
| [`onImageSourceStateReceived`](#onimagesourcestateReceived) | Called when the state of the image source changes. |

### onImageSourceStateReceived

This method is called when the state of the image source changes.

```java
default void onImageSourceStateReceived(@EnumImageSourceState int state)
```

**Parameters**

`state` The state of the image source. It is one of the values of the `EnumImageSourceState` enumeration.

**See Also**

[EnumImageSourceState]({{ site.dcvb_java_api }}capture-vision-router/enum-image-source-state.html)
