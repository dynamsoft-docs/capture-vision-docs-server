---
layout: default-layout
title: CCaptureVisionRouter Constructor and Destructor - Dynamsoft Capture Vision C++ Edition API
description: API reference for the constructor and destructor of the CCaptureVisionRouter class in Dynamsoft Capture Vision C++ Edition.
keywords: capture vision, router, instance, api reference, C++, Constructor, Destructor
needAutoGenerateSidebar: true
needGenerateH3Content: false
breadcrumbText: CVR C++ Constructor and Destructor
---

# Constructor and Destructor

| Method                                             | Description                                           |
| -------------------------------------------------- | ----------------------------------------------------- |
| [`CCaptureVisionRouter`](#ccapturevisionrouter)    | Default constructor of `CCaptureVisionRouter` object. |
| [`~CCaptureVisionRouter`](#ccapturevisionrouter-1) | Destructor of `CCaptureVisionRouter` object.          |

## CCaptureVisionRouter

Default constructor of a `CCaptureVisionRouter` object.

```cpp
CCaptureVisionRouter::CCaptureVisionRouter()
```
 
> [!IMPORTANT]
> Instances of `CCaptureVisionRouter` are not thread-safe.  
> Do not access the same `CCaptureVisionRouter` instance from multiple threads concurrently.  
> Create a separate instance for each thread if concurrent processing is required.


## ~CCaptureVisionRouter

Destructor of a `CCaptureVisionRouter` object.

```cpp
CCaptureVisionRouter::~CCaptureVisionRouter()
```
