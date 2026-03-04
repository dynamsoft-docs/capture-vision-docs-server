---
layout: default-layout
title: BufferedItemsManager Class - Dynamsoft Capture Vision Router Module Java Edition API Reference
description: API reference for the BufferedItemsManager class in Dynamsoft Capture Vision Java Edition, which manages the buffer of captured result items for cross-frame verification.
keywords: buffered items manager, java
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# BufferedItemsManager

Defines a manager for buffered items in the capture vision workflow.

## Definition

*Package:* com.dynamsoft.cvr

```java
class BufferedItemsManager
```

## Methods

| Method                                                    | Description                                        |
| --------------------------------------------------------- | -------------------------------------------------- |
| [`setMaxBufferedItems`](#setmaxbuffereditems) | Sets the maximum number of buffered items. |
| [`getMaxBufferedItems`](#getmaxbuffereditems) | Gets the maximum number of buffered items. |
| [`getBufferedCharacterItemSet`](#getbufferedcharacteritemset) | Gets the buffered recognized character items. |

### setMaxBufferedItems

Sets the maximum number of buffered items.

```java
public void setMaxBufferedItems(int count)
```

**Parameters**

`count` The maximum number of buffered items.

### getMaxBufferedItems

Gets the maximum number of buffered items.

```java
public int getMaxBufferedItems()
```

**Return value**

Returns the maximum number of buffered items.

### getBufferedCharacterItemSet

Gets the buffered recognized character items.

```java
public BufferedCharacterItemSet getBufferedCharacterItemSet()
```

**Return value**

Returns the buffered recognized character items.

**See Also**

[BufferedCharacterItemSet]({{ site.dlr_java_api }}buffered-character-item-set.html)
