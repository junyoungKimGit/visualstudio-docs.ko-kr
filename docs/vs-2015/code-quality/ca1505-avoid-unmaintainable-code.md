---
title: ': Ca1505 유지 관리할 수 없는 코드 | Microsoft Docs'
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
- AvoidUnmaintainableCode
- CA1505
helpviewer_keywords:
- AvoidUnmaintainableCode
- CA1505
ms.assetid: 8292b268-5929-4221-b699-f9c414bcec5d
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: ee836af1ee0030c3eea56e12ea5fe767c4b7255b
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/24/2018
ms.locfileid: "47591683"
---
# <a name="ca1505-avoid-unmaintainable-code"></a>CA1505: 유지 관리할 수 없는 코드는 사용하지 마십시오.
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [CA1505: 유지 관리할 수 없는 코드를 피](https://docs.microsoft.com/visualstudio/code-quality/ca1505-avoid-unmaintainable-code)합니다.

|||
|-|-|
|TypeName|AvoidUnmantainableCode|
|CheckId|CA1505|
|범주|Microsoft.Maintainability|
|변경 수준|주요 변경 아님|

## <a name="cause"></a>원인
 형식 또는 메서드에 낮은 유지 관리 인덱스 값이 있습니다.

## <a name="rule-description"></a>규칙 설명
 유지 관리 인덱스는 다음 메트릭을 사용 하 여 계산 됩니다: 줄의 코드, 프로그램 볼륨 및 순환 복잡성입니다. 프로그램 볼륨은 형식 또는 코드의 연산자 및 피연산자의 수를 기반으로 하는 방법에 대 한 이해 하기 어려운 이유는 측정값입니다. 순환 복잡성은 구조적 형식 또는 메서드의 복잡성을 측정 합니다. 코드 메트릭에 대 한 자세히 알아볼 수 있습니다 [측정 복잡성과 관리 되는 코드 관리 용이성](../code-quality/measuring-complexity-and-maintainability-of-managed-code.md)합니다.

 낮은 유지 관리 인덱스를 나타내고 형식 또는 메서드를 유지 관리 하기 어렵고 다시 디자인 좋은 후보가 됩니다.

## <a name="how-to-fix-violations"></a>위반 문제를 해결하는 방법
 이 위반을 해결 하려면 형식 또는 메서드를 다시 디자인 하 고 작고 더욱 중점을 둔 형식이 나 메서드의로 분할 하려고 합니다.

## <a name="when-to-suppress-warnings"></a>경고를 표시하지 않는 경우
 형식 또는 메서드는 여전히 크더라도 큰 크기로 나 형식 또는 메서드를 분할할 수 없는 경우 경우이 경고를 제외 합니다.

## <a name="see-also"></a>참고 항목
 [유지 관리 경고](../code-quality/maintainability-warnings.md) [복잡성 및 관리 되는 코드 관리 용이성 측정](../code-quality/measuring-complexity-and-maintainability-of-managed-code.md)


