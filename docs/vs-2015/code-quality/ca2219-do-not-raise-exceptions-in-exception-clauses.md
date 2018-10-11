---
title: 'CA2219: exception 절에서 예외를 일으키지 않습니다 | Microsoft Docs'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- DoNotRaiseExceptionsInExceptionClauses
- CA2219
helpviewer_keywords:
- DoNotRaiseExceptionsInExceptionClauses
- CA2219
ms.assetid: 7b9b0bee-4e8e-49a4-8c40-52142b49061f
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 3f3ea7368026e2e120e877a8689319762fa2b55e
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/24/2018
ms.locfileid: "47565453"
---
# <a name="ca2219-do-not-raise-exceptions-in-exception-clauses"></a>CA2219: exception 절에서 예외를 발생시키지 마십시오.
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [CA2219: exception 절에서 예외를 발생 하지 않습니다](https://docs.microsoft.com/visualstudio/code-quality/ca2219-do-not-raise-exceptions-in-exception-clauses)합니다.

|||
|-|-|
|TypeName|DoNotRaiseExceptionsInExceptionClauses|
|CheckId|CA2219|
|범주|Microsoft.Usage|
|변경 수준|아님, 주요 변경|

## <a name="cause"></a>원인
 예외가 발생 한 `finally`, 필터 또는 fault 절.

## <a name="rule-description"></a>규칙 설명
 Exception 절에서 예외가 발생 하면 디버깅 하는 것이 어렵기 크게 증가 합니다.

 예외가 발생 하는 경우는 `finally` fault 절 하면 새로운 예외가 활성 예외를 숨기 있으면 또는 합니다. 이렇게 하면 원래 오류를 발견 하 여 디버깅 하기가 어렵습니다.

 필터 절에서 예외가 발생 하면 런타임은 자동으로 예외를 catch 하 고 하면 필터가 false로 평가 합니다. False를 필터에서 throw 하는 예외 필터 평가 차이 구별할 방법이 없습니다. 이렇게 하면 검색 및 필터의 논리에서 오류를 디버깅 하기가 어렵습니다.

## <a name="how-to-fix-violations"></a>위반 문제를 해결하는 방법
 이 규칙 위반이를 해결 하려면 명시적으로 올리지 마십시오에서 예외를 `finally`, 필터 또는 fault 절.

## <a name="when-to-suppress-warnings"></a>경고를 표시하지 않는 경우
 이 규칙에 대 한 경고를 표시 하지 마십시오. exception 절에서 발생 한 예외는 코드 실행에 도움이 시나리오가 있습니다.

## <a name="related-rules"></a>관련된 규칙
 [CA1065: 예기치 않은 위치에서 예외를 발생시키지 마십시오.](../code-quality/ca1065-do-not-raise-exceptions-in-unexpected-locations.md)

## <a name="see-also"></a>참고 항목
 [디자인 경고](../code-quality/design-warnings.md)


