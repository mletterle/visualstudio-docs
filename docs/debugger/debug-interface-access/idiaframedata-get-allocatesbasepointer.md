---
description: "IDiaFrameData::get_allocatesBasePointer retrieves a flag that indicates whether the base pointer is allocated for code in this address range."
title: "IDiaFrameData::get_allocatesBasePointer"
ms.date: "11/04/2016"
ms.topic: "reference"
dev_langs:
  - "C++"
helpviewer_keywords:
  - "IDiaFrameData::get_allocatesBasePointer method"
author: "mikejo5000"
ms.author: "mikejo"
manager: mijacobs
ms.subservice: debug-diagnostics
---
# IDiaFrameData::get_allocatesBasePointer

Retrieves a flag that indicates whether the base pointer is allocated for code in this address range. This method is deprecated.

## Syntax

```C++
HRESULT get_allocatesBasePointer ( 
   BOOL* pRetVal
);
```

#### Parameters
 `pRetVal`

[out] Returns `TRUE` if a base pointer is allocated; otherwise, returns `FALSE`.

## Return Value
 If successful, returns `S_OK`. Returns `S_FALSE` if this property is not supported. Otherwise, returns an error code.

## Remarks
 This property should be used only by code that formerly accessed FPO_DATA, or when the program string returned by the [IDiaFrameData::get_program](../../debugger/debug-interface-access/idiaframedata-get-program.md) method is `NULL`. Otherwise, the program string contains all the information needed to compute previous register values.

## See also
- [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)
- [IDiaFrameData::get_program](../../debugger/debug-interface-access/idiaframedata-get-program.md)
