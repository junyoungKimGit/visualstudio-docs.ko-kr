---
title: 'IDebugObject2:: IsEncOutdated 된 | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugObject2::IsEncOutdated
helpviewer_keywords:
- IDebugObject2::IsEncOutdated method
ms.assetid: d3a8c02d-895b-478c-9957-d663130f308e
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: a90ff97b87ec2abaab87dfece5b2a2ac1cabb28c
ms.sourcegitcommit: 6cfffa72af599a9d667249caaaa411bb28ea69fd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/02/2020
ms.locfileid: "80726107"
---
# <a name="idebugobject2isencoutdated"></a>IDebugObject2::IsEncOutdated
이 메서드는이 개체 또는 부모 컨테이너의 편집 하며 계속 하기 상태가 최신이 아닌 지 여부를 확인 합니다. 사용자 지정 식 계산기는이 메서드를 구현 하지 않으며 항상를 반환 `E_NOTIMPL` 합니다.

## <a name="syntax"></a>구문

```cpp
HRESULT IsEncOutdated(
   BOOL* pfEncOutdated
);
```

```csharp
int IsEncOutdated(
   out int pfEncOutdated
);
```

## <a name="parameters"></a>매개 변수
`pfEncOutdated`\
제한이 `TRUE`편집 하며 계속 하기 상태가 오래 된 경우 0이 아닌 값이 고, `FALSE` 그렇지 않으면 0 ()입니다.

## <a name="return-value"></a>반환 값
 성공 하면이 반환 되 `S_OK` 고, 그렇지 않으면 오류 코드가 반환 됩니다.

> [!NOTE]
> 사용자 지정 식 계산기는 항상를 반환 해야 합니다 `E_NOTIMPL` .

## <a name="see-also"></a>추가 정보
- [IDebugObject2](../../../extensibility/debugger/reference/idebugobject2.md)
