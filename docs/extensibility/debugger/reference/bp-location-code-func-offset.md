---
title: BP_LOCATION_CODE_FUNC_OFFSET | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- BP_LOCATION_CODE_FUNC_OFFSET
helpviewer_keywords:
- BP_LOCATION_CODE_FUNC_OFFSET structure
ms.assetid: ab38f7ca-fa01-4cf3-a06c-56cbb7207617
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
ms.openlocfilehash: 32331a5b628c27dc79d6a2e5919c8d268c96a3aa
ms.sourcegitcommit: 6cfffa72af599a9d667249caaaa411bb28ea69fd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/02/2020
ms.locfileid: "80738001"
---
# <a name="bp_location_code_func_offset"></a>BP_LOCATION_CODE_FUNC_OFFSET
코드의 함수에서 중단점의 오프셋 위치에 대해 설명 합니다.

## <a name="syntax"></a>구문

```cpp
typedef struct _BP_LOCATION_CODE_FUNC_OFFSET {
    BSTR                     bstrContext;
    IDebugFunctionPosition2* pFuncPos;
} BP_LOCATION_CODE_FUNC_OFFSET;
```

## <a name="members"></a>멤버
`bstrContext`\
중단점의 컨텍스트 (일반적으로 호출 스택에 표시 되는 메서드 또는 함수 이름)입니다.

`pFuncPos`\
함수의 이름과 함수의 시작 부분에서의 상대 위치를 설명 하는 [IDebugFunctionPosition2](../../../extensibility/debugger/reference/idebugfunctionposition2.md) 개체입니다.

## <a name="remarks"></a>설명
이 구조체는 공용 구조체의 일부로 [BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md) 구조체의 멤버입니다.

`pFuncPos`멤버는 함수 중단점을 설정할 위치를 나타냅니다.

## <a name="requirements"></a>요구 사항
헤더: msdbg .h

네임 스페이스: VisualStudio

어셈블리: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>추가 정보
- [클래스 및 공용 구조체](../../../extensibility/debugger/reference/structures-and-unions.md)
- [BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md)
- [IDebugFunctionPosition2](../../../extensibility/debugger/reference/idebugfunctionposition2.md)
