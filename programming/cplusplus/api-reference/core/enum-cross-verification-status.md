---
layout: default-layout
title: CrossVerificationStatus - Dynamsoft Core Enumerations
description: Reference for the CrossVerificationStatus enumeration in Dynamsoft Core C++ Edition, indicating whether a result has been cross-verified across multiple frames.
keywords: cross verification status
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CrossVerificationStatus
codeAutoHeight: true
---

# Enumeration CrossVerificationStatus

`CrossVerificationStatus` describes the status of the captured results.

<div class="sample-code-prefix template2"></div>
   >- C++
   >
>
```cpp
typedef enum CrossVerificationStatus
{
    /** The cross verification has not been performed yet. */
    CVS_NOT_VERIFIED,
    /** The cross verification has been passed successfully. */
    CVS_PASSED,
    /** The cross verification has failed. */
    CVS_FAILED
} CrossVerificationStatus;
```
