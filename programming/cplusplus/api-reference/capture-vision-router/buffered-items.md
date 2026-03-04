---
layout: default-layout
title: CaptureVisionRouter Buffered Items - Dynamsoft Capture Vision C++ Edition API
description: API reference for the buffered items method of CCaptureVisionRouter in Dynamsoft Capture Vision C++ Edition, returning the BufferedItemsManager for managing buffered character items.
keywords: capture vision, buffered items, instance, api reference, C++
needAutoGenerateSidebar: true
needGenerateH3Content: false
breadcrumbText: CVR C++ Buffered Items
---

# Buffered Items

| API Name                                                      | Description                                               |
| ------------------------------------------------------------- | --------------------------------------------------------- |
| [`GetBufferedItemsManager`](#getbuffereditemsmanager)               | Gets the manager instance of buffered items.         |

## GetBufferedItemsManager

Gets the manager instance of buffered items.

```cpp
CBufferedItemsManager* GetBufferedItemsManager();
```

**Return Value**

Returns the manager instance of buffered items.

**Remarks**

When the maximum number of buffered items is set to greater than 0, item buffering is enabled. Currently only character items can be buffered.
