---
layout: default-layout
title: class CBufferedItemsManager - Dynamsoft Capture Vision Router Module C++ Edition API Reference
description: This page shows the C++ edition of the class CBufferedItemsManager in Dynamsoft Capture Vision Router Module.
keywords: buffered items manager, c++
needAutoGenerateSidebar: true
---

# CBufferedItemsManager

The `CBufferedItemsManager` class is used to manage the buffered items. It provides methods to get and set the maximum number of buffer items and to get buffer items.

## Definition

*Namespace:* dynamsoft::cvr

*Assembly:* DynamsoftCaptureVisionRouter

```cpp
class CBufferedItemsManager 
```

## Methods

| Method | Description |
|--------|-------------|
| [`SetMaxBufferedItems`](#setmaxbuffereditems) | Sets the maximum number of buffered items.|
| [`GetMaxBufferedItems`](#getmaxbuffereditems) | Gets the maximum number of buffered items. |
| [`GetBufferedCharacterItemSet`](#getbufferedcharacteritemset) | Gets the buffered recognized character items. |

### SetMaxBufferedItems

Sets the maximum number of buffered items.

```cpp
virtual void SetMaxBufferedItems(int count)
```

**Parameters**

`[in] count` The maximum number of buffered items.

### GetMaxBufferedItems

Gets the maximum number of buffered items.

```cpp
virtual int GetMaxBufferedItems() const
```

**Return value**

Returns the maximum number of buffered items.

### GetBufferedCharacterItemSet

Gets the buffered recognized character items.

```cpp
virtual CBufferedCharacterItemSet* GetBufferedCharacterItemSet() const
```

**Return value**

Returns the buffered recognized character items.

**See Also**

[CBufferedCharacterItemSet]({{ site.dlr_cpp_api }}buffered-character-item-set.html)
