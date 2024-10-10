---
layout: default-layout
title: IImageSourceErrorListener Interface - Dynamsoft Capture Vision Module .NET Edition API Reference
description: Definition of IImageSourceErrorListener interface in Dynamsoft Core Module .NET Edition.
keywords: imagesource error listener, .NET
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# IImageSourceErrorListener

The `IImageSourceErrorListener` interface defines a listener for receiving error notifications from an image source.

## Definition

*Namespace:* Dynamsoft.Core

*Assembly:* Dynamsoft.Core.dll

```csharp
public interface IImageSourceErrorListener 
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`OnErrorReceived`](#onerrorreceived) | Called when an error is received from the image source. |

### OnErrorReceived

Called when an error is received from the image source.

```csharp
void OnErrorReceived(int errorCode, string errorMessage)
```

**Parameters**

`[in] errorCode` The integer error code indicating the type of error.

`[in] errorMessage` A C-style string containing the error message providing additional information about the error.

**See Also**

[EnumErrorCode]({{ site.dcvb_enumerations }}core/error-code.html?lang=dotnet)
