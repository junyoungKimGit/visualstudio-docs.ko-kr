---
title: 'IDebugProcessEx2:: Attach | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProcessEx2::Attach
helpviewer_keywords:
- IDebugProcessEx2::Attach method
ms.assetid: f3334ed7-39bf-4d02-a338-36f567b9b287
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: d70da2530a1677367a22968436a17eba809fd24a
ms.sourcegitcommit: 6cfffa72af599a9d667249caaaa411bb28ea69fd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/02/2020
ms.locfileid: "80723388"
---
# <a name="idebugprocessex2attach"></a>IDebugProcessEx2::Attach
이 메서드는 세션이 프로세스를 디버깅 하 고 있음을 프로세스에 알립니다.

## <a name="syntax"></a>구문

```cpp
HRESULT Attach( 
   IDebugSession2* pSession
);
```

```csharp
int Attach(
   IDebugSession2 pSession
);
```

## <a name="parameters"></a>매개 변수
`pSession`\
진행 이 프로세스에 연결 되는 세션을 고유 하 게 식별 하는 값입니다.

## <a name="return-value"></a>반환 값
 성공 하면이 반환 되 `S_OK` 고, 그렇지 않으면 오류 코드가 반환 됩니다.

## <a name="remarks"></a>설명
 전달 된 인터페이스는 `pSession` 이 프로세스에 연결 되는 세션 디버그 관리자를 고유 하 게 식별 하는 값인 쿠키로만 처리 됩니다. 제공 된 인터페이스의 메서드는 작동 하지 않습니다.

## <a name="see-also"></a>추가 정보
- [IDebugProcessEx2](../../../extensibility/debugger/reference/idebugprocessex2.md)
