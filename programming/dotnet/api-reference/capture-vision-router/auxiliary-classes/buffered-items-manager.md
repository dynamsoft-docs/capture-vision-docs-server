---
layout: default-layout
title: class BufferedItemsManager - Dynamsoft Capture Vision Router Module .NET Edition API Reference
description: This page shows the .NET Edition of the class BufferedItemsManager in Dynamsoft Capture Vision Router Module.
keywords: buffered items manager, .NET
needAutoGenerateSidebar: true
---

# BufferedItemsManager

The `BufferedItemsManager` class is used to manage the buffered items. It provides methods to get and set the maximum number of buffer items and to get buffer items.

## Definition

*Namespace:* Dynamsoft.CVR


```csharp
public class BufferedItemsManager 
```

## Methods

| Method | Description |
|--------|-------------|
| [`SetMaxBufferedItems`](#setmaxbuffereditems) | Sets the maximum number of buffered items.|
| [`GetMaxBufferedItems`](#getmaxbuffereditems) | Gets the maximum number of buffered items. |
| [`GetBufferedCharacterItemSet`](#getbufferedcharacteritemset) | Gets the buffered recognized character items. |

### SetMaxBufferedItems

Sets the maximum number of buffered items.

```csharp
void SetMaxBufferedItems(int count)
```

**Parameters**

`[in] count` The maximum number of buffered items.

### GetMaxBufferedItems

Gets the maximum number of buffered items.

```csharp
int GetMaxBufferedItems()
```

**Return value**

Returns the maximum number of buffered items.

### GetBufferedCharacterItemSet

Gets the buffered recognized character items.

```csharp
BufferedCharacterItemSet GetBufferedCharacterItemSet()
```

**Return value**

Returns the buffered recognized character items.

**See Also**

[BufferedCharacterItemSet]({{ site.dlr_dotnet_api }}buffered-character-item-set.html)
