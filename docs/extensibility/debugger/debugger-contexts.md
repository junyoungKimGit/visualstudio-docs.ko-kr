---
title: 디버거 컨텍스트 | Microsoft Docs
description: Visual Studio 디버그 엔진이 코드 컨텍스트, 설명서 컨텍스트, 위치 및 식 계산 컨텍스트 내에서 작동 하는 방법에 대해 알아봅니다.
ms.custom: SEO-VS-2020
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], contexts
ms.assetid: 79808036-b680-4e4c-9c61-4ed43aa11323
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 355ca667f0f909ebedc6f404ded545b3f862a444
ms.sourcegitcommit: 8e9c38da7bcfbe9a461c378083846714933a0e1e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/09/2020
ms.locfileid: "96914688"
---
# <a name="debugger-contexts"></a>디버거 컨텍스트
[!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]디버깅에서 디버그 엔진 (DE)은 다음과 같이 여러 개의 고유 컨텍스트 내에서 동시에 작동 합니다.

- 프로그램의 실행 스트림에서 현재 위치를 설명 하는 코드 컨텍스트입니다.

- 소스 문서 내의 현재 위치를 설명 하는 설명서 컨텍스트 또는 위치입니다.

- 식 계산 컨텍스트는 식 계산을 수행할 컨텍스트를 설명 합니다.

## <a name="in-this-section"></a>섹션 내용
 [코드 컨텍스트](../../extensibility/debugger/code-context.md) 오늘날의 런타임 아키텍처와 특수 언어에서 프로그램의 명령 스트림의 주소로 코드 컨텍스트를 설명 합니다. 여기서 코드는 명령으로 표시 될 수 없지만 다른 몇 가지 방법이 있습니다.

 [문서 위치](../../extensibility/debugger/document-position.md) IDE에 알려진 소스 파일의 위치에 대 한 추상화를 통해 Visual Studio 디버깅의 문서 위치를 정의 합니다.

 [문서 컨텍스트](../../extensibility/debugger/document-context.md) 소스 파일을 기준으로 Visual Studio 디버깅에서 문서 컨텍스트가 나타내는 내용에 대해 설명 합니다. 기호 처리기가 코드 컨텍스트를 설명서 컨텍스트에 매핑하는 방법도 설명 합니다.

 [식 계산 컨텍스트](../../extensibility/debugger/expression-evaluation-context.md) Visual Studio의 식 계산 컨텍스트에 대 한 정보를 제공 합니다. 예를 들어 스택 프레임과 연결 된 식 계산 컨텍스트는 지역 변수, 메서드 매개 변수 및 클래스 멤버를 평가 하기 위한 컨텍스트를 제공 합니다.

## <a name="related-sections"></a>관련 단원
 [디버그 개념](../../extensibility/debugger/debugger-concepts.md) 주요 디버깅 아키텍처 개념을 설명 합니다.

 [구성 요소 디버그](../../extensibility/debugger/debugger-components.md) 디버그 엔진 (DE), 식 계산기 (EE) 및 기호 처리기 (SH)를 포함 하는 Visual Studio 디버깅 구성 요소에 대 한 개요를 제공 합니다.

 [디버그 작업](../../extensibility/debugger/debugging-tasks.md) 프로그램 시작 및 식 계산과 같은 다양 한 디버깅 태스크에 대 한 링크를 포함 합니다.
