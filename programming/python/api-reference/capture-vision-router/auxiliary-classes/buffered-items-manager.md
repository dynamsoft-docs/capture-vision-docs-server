---
layout: default-layout
title: BufferedItemsManager Class - Dynamsoft Capture Vision Router Module Python Edition API Reference
description: Definition of BufferedItemsManager class in Dynamsoft Capture Vision Module Python Edition.
keywords: buffered items manager, python
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# BufferedItemsManager

BufferedItemsManager class is used to manage the buffered items. It provides methods to get and set the maximum number of buffer items and to get buffer items.

## Definition

*Module:* dynamsoft_capture_vision_router

```python
class BufferedItemsManager
```

## Methods

| Method                                                    | Description                                        |
| --------------------------------------------------------- | -------------------------------------------------- |
| [`set_max_buffered_items_count`](#set_max_buffered_items_count) | Sets the maximum number of buffered items. |
| [`get_max_buffered_items_count`](#set_max_buffered_items_count) | Gets the maximum number of buffered items. |
| [`get_buffered_character_item_set`](#set_max_buffered_items_count) | Gets the buffered recognized character items. |

### set_max_buffered_items_count

Sets the maximum number of buffered items.

```python
def set_max_buffered_items_count(self, count: int) -> None:
```

**Parameters**

`count` The maximum number of buffered items.

### get_max_buffered_items_count

Gets the maximum number of buffered items.

```python
def get_max_buffered_items_count(self) -> int:
```

**Return value**

Returns the maximum number of buffered items.

### get_buffered_character_item_set

Gets the buffered recognized character items.

```python
def get_buffered_character_item_set(self) -> "BufferedCharacterItemSet":
```

**Return value**

Returns the buffered recognized character items.

**See Also**

[BufferedCharacterItemSet]({{ site.dlr_python_api }}buffered-character-item-set.html)
