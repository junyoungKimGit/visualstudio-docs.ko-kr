---
title: IDebugPointerObject::D ereference | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPointerObject::Dereference
helpviewer_keywords:
- IDebugPointerObject::Dereference method
ms.assetid: 196ec2cc-8569-4780-b217-23b24e7f50ca
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: fe87d5db40ce663d84c9561e89a84e6fcb1684ed
ms.sourcegitcommit: 6cfffa72af599a9d667249caaaa411bb28ea69fd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/02/2020
ms.locfileid: "80725570"
---
# <a name="idebugpointerobjectdereference"></a>IDebugPointerObject::Dereference
가리키는 개체를 가져옵니다.

## <a name="syntax"></a>구문

```cpp
HRESULT DeReference( 
   DWORD          dwIndex,
   IDebugObject** ppObject
);
```

```csharp
int Dereference(
   uint             dwIndex,
   out IDebugObject ppObject
);
```

## <a name="parameters"></a>매개 변수
`dwIndex`\
진행 가 가리키는 개체의 시작 부분에서의 단순 바이트 오프셋입니다.

`ppObject`\
제한이 가리키는 개체를 나타내는 [Idebugobject](../../../extensibility/debugger/reference/idebugobject.md) 개체와 offset (있는 경우)을 반환 합니다.

## <a name="return-value"></a>반환 값
 성공 하면 S_OK을 반환 합니다. 그렇지 않으면 오류 코드를 반환 합니다. 이 개체가 다른 개체를 가리키지 않는 경우 E_FAIL를 반환 합니다.

## <a name="remarks"></a>설명
 가리키는 개체는 기본 형식 이거나 클래스 또는 구조체와 같은 더 복잡 한 형식일 수 있습니다.

## <a name="see-also"></a>추가 정보
- [IDebugPointerObject](../../../extensibility/debugger/reference/idebugpointerobject.md)
