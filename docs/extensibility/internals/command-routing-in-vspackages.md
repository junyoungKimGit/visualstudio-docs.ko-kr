---
title: Vspackage에서 명령 라우팅 | Microsoft Docs
description: Vspackage의 명령 라우팅과 Visual Studio에서 실행 되는 컨텍스트에 따라 명령이 라우팅되는 방법에 대해 알아봅니다.
ms.custom: SEO-VS-2020
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- commands, routing
- command routing, Visual Studio SDK
ms.assetid: a9c7f9ae-3594-4557-a314-8cf76f5f8772
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8168fbe3ad5ba9b1b332aebc4675ecd8e752ee7e
ms.sourcegitcommit: 2244665d5a0e22d12dd976417f2a782e68684705
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/28/2020
ms.locfileid: "96305223"
---
# <a name="command-routing-in-vspackages"></a>Vspackage의 명령 라우팅
명령은 [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] 실행 되는 컨텍스트를 기반으로에서 라우팅됩니다. 초기 컨텍스트에서 전역 컨텍스트로 외부로 라우팅됩니다.

## <a name="in-this-section"></a>섹션 내용
- [명령 라우팅 알고리즘](../../extensibility/internals/command-routing-algorithm.md)

 명령 라우팅 확인 순서를 설명 합니다.

- [명령 가용성](../../extensibility/internals/command-availability.md)

 명령 라우팅에 대해 설명 합니다.

- [Interop 어셈블리를 사용 하는 명령 및 메뉴](../../extensibility/internals/commands-and-menus-that-use-interop-assemblies.md)

 관리 코드와 COM 간의 라우팅 명령에 대 한 고려 사항을 설명 합니다.

## <a name="related-sections"></a>관련 단원
- [선택 컨텍스트 개체](../../extensibility/internals/selection-context-objects.md)

 창에서 사용자의 선택 컨텍스트 포커스를 확인할 수 있는 방법에 대 한 모델을 설명 합니다.

- [명령, 메뉴 및 도구 모음](../../extensibility/internals/commands-menus-and-toolbars.md)

 메뉴, 도구 모음 및 명령 콤보 상자를 포함하는 UI를 만드는 방법을 설명합니다.
