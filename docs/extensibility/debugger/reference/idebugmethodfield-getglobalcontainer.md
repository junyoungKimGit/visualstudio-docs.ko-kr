---
title: 'IDebugMethodField:: GetGlobalContainer | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugMethodField::GetGlobalContainer
helpviewer_keywords:
- IDebugMethodField::GetGlobalContainer method
ms.assetid: 041ac5aa-0b80-4310-b9ae-b88f8e7e0e5f
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 37e3b26a265fe651216e46fa299bdd827416b8ce
ms.sourcegitcommit: 6cfffa72af599a9d667249caaaa411bb28ea69fd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/02/2020
ms.locfileid: "80727129"
---
# <a name="idebugmethodfieldgetglobalcontainer"></a>IDebugMethodField::GetGlobalContainer
메서드의 전역 컨테이너를 가져옵니다.

## <a name="syntax"></a>구문

```cpp
HRESULT GetGlobalContainer(
   IDebugClassField** ppClass
);
```

```csharp
int GetGlobalContainer(
   out IDebugClassField ppClass
);
```

## <a name="parameters"></a>매개 변수
`ppClass`\
제한이 이 메서드가 정의 된 모듈을 나타내는 [Idebugclassfield](../../../extensibility/debugger/reference/idebugclassfield.md) 를 반환 합니다.

## <a name="return-value"></a>반환 값
 성공 하면 S_OK을 반환 합니다. 그렇지 않으면 오류 코드를 반환 합니다.

## <a name="remarks"></a>설명
 반환 된 [Idebugclassfield](../../../extensibility/debugger/reference/idebugclassfield.md) 개체는 전체 모듈을 나타내며 인공 개체입니다. 즉, 모듈 자체에 실제 클래스가 없지만 개체로 나타낼 수 있으므로 `IDebugClassField` 모듈의 다양 한 요소를 열거 하 고 검색할 수 있습니다.

## <a name="see-also"></a>추가 정보
- [IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md)
- [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md)
