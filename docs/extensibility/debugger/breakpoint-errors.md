---
title: 중단점 오류 | Microsoft Docs
description: 중단점이 코드에 바인딩하려는 경우 프로세스에 대해 알아보고 실패 하 고 중단점 오류를 해결 하는 방법을 알아봅니다.
ms.custom: SEO-VS-2020
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- breakpoints, errors
- debugging [Debugging SDK], breakpoint errors
- errors [Debugging SDK]
ms.assetid: 79221c6b-a924-4c8e-a778-e312e4e0c0c8
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 88a5003ce8abe79fcba9f9604047d2265810fda2
ms.sourcegitcommit: 8e9c38da7bcfbe9a461c378083846714933a0e1e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/09/2020
ms.locfileid: "96914493"
---
# <a name="breakpoint-errors"></a>중단점 오류
다음은 중단점에서 코드에 바인딩하려고 하지만 실패 하는 경우의 프로세스에 대 한 설명입니다.

## <a name="troubleshoot-a-breakpoint-error"></a>중단점 오류 문제 해결

1. DE (디버그 엔진)는 [IDebugBreakpointErrorEvent2](../../extensibility/debugger/reference/idebugbreakpointerrorevent2.md) 을 세션 디버그 관리자 (SDM)로 보냅니다.

2. SDM은 [IDebugBreakpointErrorEvent2:: GetErrorBreakpoint](../../extensibility/debugger/reference/idebugbreakpointerrorevent2-geterrorbreakpoint.md) (IDebugErrorBreakpoint2 * * `ppErrorBP` )를 호출 하 여 오류 중단점을 가져옵니다.

3. SDM은 [IDebugErrorBreakpoint2:: GetPendingBreakpoint](../../extensibility/debugger/reference/idebugerrorbreakpoint2-getpendingbreakpoint.md) 을 호출 하 여 오류 중단점이 시작 된 보류 중인 중단점을 가져옵니다.

4. SDM은 [IDebugErrorBreakpoint2:: GetBreakpointResolution](../../extensibility/debugger/reference/idebugerrorbreakpoint2-getbreakpointresolution.md) 을 호출 하 여 오류 중단점을 바인딩하지 못한 이유를 가져옵니다.

## <a name="see-also"></a>참고 항목
- [디버거 이벤트 호출](../../extensibility/debugger/calling-debugger-events.md)
