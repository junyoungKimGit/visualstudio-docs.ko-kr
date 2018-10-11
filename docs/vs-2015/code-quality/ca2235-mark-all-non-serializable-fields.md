---
title: 'CA2235: 모두 순차 불가능 필드로 표시 | Microsoft Docs'
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
- CA2235
- MarkAllNonSerializableFields
helpviewer_keywords:
- CA2235
- MarkAllNonSerializableFields
ms.assetid: 599ad877-3a15-426c-bf17-5de15427365f
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 025ee336052bdad010b55e1ba804b2bd37c7e0d7
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/24/2018
ms.locfileid: "47591748"
---
# <a name="ca2235-mark-all-non-serializable-fields"></a>CA2235: 모두 serialize할 수 없는 필드로 표시하십시오.
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [CA2235: 모든 순차 불가능 필드를 표시할](https://docs.microsoft.com/visualstudio/code-quality/ca2235-mark-all-non-serializable-fields)합니다.

|||
|-|-|
|TypeName|MarkAllNonSerializableFields|
|CheckId|CA2235|
|범주|Microsoft.Usage|
|변경 수준|주요 변경 아님|

## <a name="cause"></a>원인
 serialize할 수 없는 형식의 인스턴스 필드가 serialize할 수 있는 형식에 정의되었습니다.

## <a name="rule-description"></a>규칙 설명
 직렬화 가능 형식 것으로 표시 되는 <xref:System.SerializableAttribute?displayProperty=fullName> 특성입니다. 형식으로 serialize 될 때를 <xref:System.Runtime.Serialization.SerializationException?displayProperty=fullName> 형식을 직렬화 할 수 없는 형식의 인스턴스 필드를 포함 하는 경우 예외가 throw 됩니다.

## <a name="how-to-fix-violations"></a>위반 문제를 해결하는 방법
 이 규칙 위반 문제를 해결 하려면 적용 된 <xref:System.NonSerializedAttribute?displayProperty=fullName> 특성을 직렬화 할 수 없는 필드입니다.

## <a name="when-to-suppress-warnings"></a>경고를 표시하지 않는 경우
 경우에이 규칙에서 경고를 표시는 <xref:System.Runtime.Serialization.ISerializationSurrogate?displayProperty=fullName> 형식이 serialize 및 deserialize 될 필드의 인스턴스를 허용 하는 선언 되었습니다.

## <a name="example"></a>예제
 다음 예제에서는 규칙을 위반 하는 형식을 규칙을 충족 하는 형식을 보여 줍니다.

 [!code-csharp[FxCop.Usage.MarkNonSerializable#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.MarkNonSerializable/cs/FxCop.Usage.MarkNonSerializable.cs#1)]
 [!code-vb[FxCop.Usage.MarkNonSerializable#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Usage.MarkNonSerializable/vb/FxCop.Usage.MarkNonSerializable.vb#1)]

## <a name="related-rules"></a>관련된 규칙
 [CA2236: ISerializable 형식에서 기본 클래스 메서드를 호출하십시오.](../code-quality/ca2236-call-base-class-methods-on-iserializable-types.md)

 [CA2240: ISerializable을 올바르게 구현하십시오.](../code-quality/ca2240-implement-iserializable-correctly.md)

 [CA2229: serialization 생성자를 구현하십시오.](../code-quality/ca2229-implement-serialization-constructors.md)

 [CA2238: serialization 메서드를 올바르게 구현하십시오.](../code-quality/ca2238-implement-serialization-methods-correctly.md)

 [CA2237: ISerializable 형식을 SerializableAttribute로 표시하십시오.](../code-quality/ca2237-mark-iserializable-types-with-serializableattribute.md)

 [CA2239: 선택적 필드에 deserialization 메서드를 제공하십시오.](../code-quality/ca2239-provide-deserialization-methods-for-optional-fields.md)

 [CA2120: serialization 생성자를 안전하게 하십시오.](../code-quality/ca2120-secure-serialization-constructors.md)


