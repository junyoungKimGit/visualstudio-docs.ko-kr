---
title: 'IEnumDebugPrograms2:: Skip | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumDebugPrograms2::Skip
helpviewer_keywords:
- IEnumDebugPrograms2::Skip
ms.assetid: b283858b-b375-4760-bfec-ab37de89958d
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 7459e6dae6487fbb9cec3e82a9d8ba01fbfef2a7
ms.sourcegitcommit: 6cfffa72af599a9d667249caaaa411bb28ea69fd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/02/2020
ms.locfileid: "80715598"
---
# <a name="ienumdebugprograms2skip"></a>IEnumDebugPrograms2::Skip
지정 된 수의 요소를 건너뜁니다.

## <a name="syntax"></a>구문

```cpp
HRESULT Skip(
   ULONG celt
);
```

```csharp
int Skip(
   uint celt
);
```

## <a name="parameters"></a>매개 변수
`celt`\
진행 건너뛸 요소 수입니다.

## <a name="return-value"></a>반환 값
 성공하면 `S_OK`를 반환합니다. `S_FALSE` `celt` 가 나머지 요소 수보다 크면를 반환 하 고, 그렇지 않으면 오류 코드를 반환 합니다.

## <a name="remarks"></a>설명
 가 `celt` 나머지 요소 수보다 큰 값을 지정 하는 경우 열거형은 end로 설정 되 고 `S_FALSE` 이 반환 됩니다.

## <a name="see-also"></a>추가 정보
- [IEnumDebugPrograms2](../../../extensibility/debugger/reference/ienumdebugprograms2.md)
