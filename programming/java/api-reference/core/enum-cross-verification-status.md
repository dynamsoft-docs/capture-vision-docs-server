---
layout: default-layout
title: CrossVerificationStatus - Dynamsoft Core Java Enumerations
description: The enumeration CrossVerificationStatus of Dynamsoft Core describes the status of the captured results.
keywords: cross verification status
codeAutoHeight: true
---

# Enumeration CrossVerificationStatus

`CrossVerificationStatus` describes the status of the captured results.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumCrossVerificationStatus {
    //The cross verification has not been performed yet.
    int CVS_NOT_VERIFIED = 0;
    //The cross verification has been passed successfully.
    int CVS_PASSED = 1;
    //The cross verification has failed.
    int CVS_FAILED = 2;
}
```
