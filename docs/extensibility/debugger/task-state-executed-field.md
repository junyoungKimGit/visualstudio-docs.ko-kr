---
title: TASK_STATE_EXECUTED 필드 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- TASK_STATE_EXECUTED field, Task class [.NET Framework debug engines]
ms.assetid: 75b8f9d0-b908-40d0-b109-70feaed2ab0c
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: aa637b8bc29f53ca6dde1b13310d83a5e176408f
ms.sourcegitcommit: 6cfffa72af599a9d667249caaaa411bb28ea69fd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/02/2020
ms.locfileid: "80712693"
---
# <a name="task_state_executed-field"></a>TASK_STATE_EXECUTED 필드
작업이 실행되고 있지만 완료되지 않았습니다.

 **네임스페이스:** <xref:System.Threading.Tasks?displayProperty=fullName>

 **어셈블리:** mscorlib (mscorlib.dll)

 .NET Framework에서이 내부 멤버에 액세스할 수 없기 때문에 다음 구문이 CIL (공용 중간 언어)에서 제공 됩니다.

## <a name="syntax"></a>구문

```csharp
.field static assembly literal int32 TASK_STATE_EXECUTED = int32(0x00020000)
```

## <a name="remarks"></a>설명
 [M_stateFlags](../../extensibility/debugger/m-stateflags-field.md) 필드에이 값이 포함 되어 있으면 <xref:System.Threading.Tasks.Task.Status%2A> 속성은을 반환 합니다 <xref:System.Threading.Tasks.TaskStatus?displayProperty=fullName> .

## <a name="see-also"></a>참고 항목
- [Task 클래스](../../extensibility/debugger/task-class-internal-members.md)
