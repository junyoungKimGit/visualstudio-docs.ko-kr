---
title: PENDING_BP_STATE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- PENDING_BP_STATE
helpviewer_keywords:
- PENDING_BP_STATE enumeration
ms.assetid: ac04ad72-fa92-4a15-ade2-0d0bbbadfc7f
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 69c8dbe1022ee0b1b2ff034d2b83b947c8fb3df6
ms.sourcegitcommit: 6cfffa72af599a9d667249caaaa411bb28ea69fd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/02/2020
ms.locfileid: "80714004"
---
# <a name="pending_bp_state"></a>PENDING_BP_STATE
보류 중인 중단점 (아직 바인딩되지 않은 중단점)의 상태를 지정 합니다.

## <a name="syntax"></a>Syntax

```cpp
enum enum_PENDING_BP_STATE { 
   PBPS_NONE     = 0x0000,
   PBPS_DELETED  = 0x0001,
   PBPS_DISABLED = 0x0002,
   PBPS_ENABLED  = 0x0003
};
typedef DWORD PENDING_BP_STATE;
```

```csharp
public enum enum_PENDING_BP_STATE { 
   PBPS_NONE     = 0x0000,
   PBPS_DELETED  = 0x0001,
   PBPS_DISABLED = 0x0002,
   PBPS_ENABLED  = 0x0003
};
```

## <a name="fields"></a>필드
 `PBPS_NONE`\
 0에 대 한 자리 표시자입니다. 이 값은 반환 되지 않습니다.

 `PBPS_DELETED`\
 보류 중인 중단점이 삭제 되었음을 나타냅니다.

 `PBPS_DISABLED`\
 보류 중인 중단점을 사용할 수 없음을 나타냅니다.

 `PBPS_ENABLED`\
 보류 중인 중단점을 사용할 수 있음을 나타냅니다.

## <a name="remarks"></a>설명
 `state` [PENDING_BP_STATE_INFO](../../../extensibility/debugger/reference/pending-bp-state-info.md) 구조체의 멤버로 사용 합니다.

## <a name="requirements"></a>요구 사항
 헤더: msdbg .h

 네임 스페이스: VisualStudio

 어셈블리: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>참조
- [열거형](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [PENDING_BP_STATE_INFO](../../../extensibility/debugger/reference/pending-bp-state-info.md)
