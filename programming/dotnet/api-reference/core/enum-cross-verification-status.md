---
layout: default-layout
title: CrossVerificationStatus - Dynamsoft Core .NET Enumerations
description: The enumeration CrossVerificationStatus in Dynamsoft Core .NET Edition indicates whether a captured result has been cross-verified across multiple frames.
keywords: cross verification status
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
codeAutoHeight: true
---

# Enumeration CrossVerificationStatus

`CrossVerificationStatus` describes the cross verification status of the captured results.

```csharp
public enum EnumCrossVerificationStatus
{
    /** The cross verification has not been performed yet. */
    CVS_NOT_VERIFIED,
    /** The cross verification has been passed successfully. */
    CVS_PASSED,
    /** The cross verification has failed. */
    CVS_FAILED
}
```
