---
layout: default-layout
title: IImageSourceStateListener Interface - Dynamsoft Capture Vision Router Module .NET Edition API Reference
description: API reference for the IImageSourceStateListener interface in Dynamsoft Capture Vision .NET Edition, which receives notifications when the image source state changes.
keywords: image source state listener, .NET
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# IImageSourceStateListener

Defines a listener for image source state changes.

## Definition

*Namespace:* Dynamsoft.CVR


```csharp
public interface IImageSourceStateListener 
```

## Methods

| Method                                                    | Description                                        |
| --------------------------------------------------------- | -------------------------------------------------- |
| [`OnImageSourceStateReceived`](#onimagesourcestatereceived) | Called when the state of the image source changes. |

### OnImageSourceStateReceived

This method is called when the state of the image source changes.

```csharp
void OnImageSourceStateReceived(EnumImageSourceState state)
```

**Parameters**

`[in] state` The state of the image source.

**See Also**

[EnumImageSourceState]({{ site.dcvb_dotnet_api }}capture-vision-router/enum-image-source-state.html)
