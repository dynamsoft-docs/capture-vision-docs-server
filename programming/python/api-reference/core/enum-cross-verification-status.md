---
layout: default-layout
title: CrossVerificationStatus - Dynamsoft Core Enumerations
description: The enumeration CrossVerificationStatus in Dynamsoft Core Python Edition indicates whether a captured result has been cross-verified across multiple frames.
keywords: cross verification status
codeAutoHeight: true
---

# Enumeration CrossVerificationStatus

`CrossVerificationStatus` describes the status of the captured results.

```python
class EnumCrossVerificationStatus(IntEnum):
    # The cross verification has not been performed yet.
    CVS_NOT_VERIFIED,
    # The cross verification has been passed successfully.
    CVS_PASSED,
    # The cross verification has failed.
    CVS_FAILED
```
