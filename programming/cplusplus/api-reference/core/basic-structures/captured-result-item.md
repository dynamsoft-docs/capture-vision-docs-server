---
layout: default-layout
title: class CCapturedResultItem - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CCapturedResultItem in Dynamsoft Core Module.
keywords: captured result item, c++
needAutoGenerateSidebar: true
---

# CCapturedResultItem

The CCapturedResultItem class represents an item in a captured result. It is an abstract base class with multiple subclasses, each representing a different type of captured item such as barcode, text line, detected quad, normalized image, raw image, parsed item, etc.

## Definition

*Namespace:* dynamsoft::basic_structures

*Assembly:* DynamsoftCore

```cpp
class CCapturedResultItem 
```

## Methods Summary

| Method                         | Description|
|--------------------------------|------------|
| [`~CCapturedResultItem`](#ccapturedresultitem-destructor) | This is the class destructor. |
| [`GetType`](#gettype)              | Gets the type of the captured result item. |
| [`GetReferenceItem`](#getreferenceitem)    | Gets a pointer to the referenced item in the captured result. |
| [`GetTargetROIDefName`](#gettargetroidefname) | Gets the name of the target ROI definition. |
| [`GetTaskName`](#gettaskname) | Gets the name of the task. |
| [`Retain`](#retain) | Increases the reference count of the `CCapturedResultItem` object. |
| [`Release`](#release) | Decreases the reference count of the `CCapturedResultItem` object. |
| [`Clone`](#clone) | Clone the captured result item. |

### CCapturedResultItem Destructor

This is the class destructor.

```cpp
virtual ~CCapturedResultItem(){};
```

### GetType

Gets the type of the captured result item.

```cpp
virtual CapturedResultItemType GetType() const
```

**Return value**

Returns the type of the captured result item.

**See Also**

[CapturedResultItemType]({{ site.dcv_enumerations }}core/captured-result-item-type.html?src=cpp&&lang=cpp)

### GetReferenceItem

Gets a pointer to the referenced item in the captured result item.

```cpp
virtual const CCapturedResultItem* GetReferenceItem() const
```

**Return value**

Returns a pointer to the referenced item in the captured result item. You are not required to release the memory pointed to by the returned pointer.

**See Also**

[CCapturedResultItem]({{ site.dcv_cpp_api }}core/basic-structures/captured-result-item.html)

## GetTargetROIDefName

Gets the name of the target ROI definition.

```cpp
virtual const char* GetTargetROIDefName() const = 0;
```

**Return value**

Returns the name of the target ROI definition.

## GetTaskName

Gets the name of the task.

```cpp
virtual const char* GetTaskName() const = 0;
```

**Return value**

Returns the name of the task.

## Retain

Increases the reference count of the `CCapturedResultItem` object.

```cpp
virtual CCapturedResultItem* Retain() = 0;
```

**Return value**

Returns the object of `CCapturedResultItem` with its reference count incremented.

**Remarks**

Don't forget to invoke the `Release` method when you no longer need the object.

## Release

Decreases the reference count of the `CCapturedResultItem` object.

```cpp
virtual void Release() = 0;
```

### Clone

Clones the captured result item.

```cpp
virtual CCapturedResultItem* Clone() const = 0;
```

**Return value**

Returns a pointer to a copy of the captured result item.

**Remarks**

Don't forget to invoke the `Release` method when you no longer need the object.
