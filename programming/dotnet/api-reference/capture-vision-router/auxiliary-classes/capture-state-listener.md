---
layout: default-layout
title: ICaptureStateListener Interface - Dynamsoft Capture Vision Module .NET Edition API Reference
description: Definition of ICaptureStateListener interface in Dynamsoft Capture Vision Module .NET Edition.
keywords: capture state listener, .NET
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# ICaptureStateListener

Defines a listener for capture state changes. 

## Definition

*Namespace:* Dynamsoft.CVR

*Assembly:* Dynamsoft.CaptureVisionRouter.dll

```csharp
public interface ICaptureStateListener
```

## Methods

| Method                                            | Description                            |
| ------------------------------------------------- | -------------------------------------- |
| [`OnCaptureStateChanged`](#oncapturestatechanged) | Called when the capture state changes. |

### OnCaptureStateChanged

Called when the capture state changes.

```csharp
void OnCaptureStateChanged(EnumCaptureState state)
```

**Parameters**

`[in] state` The new capture state.

**See Also**

[EnumCaptureState]({{ site.dcvb_enumerations }}capture-vision-router/capture-state.html?lang=dotnet)
