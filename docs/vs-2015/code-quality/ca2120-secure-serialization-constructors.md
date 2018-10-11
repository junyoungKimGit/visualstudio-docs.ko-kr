---
title: 'CA2120: serialization 생성자를 보안 | Microsoft Docs'
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
- CA2120
- SecureSerializationConstructors
helpviewer_keywords:
- SecureSerializationConstructors
- CA2120
ms.assetid: e9989da1-55a0-43f8-9aa9-da86afae3b41
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 6ab2a0774e813b7064aa97c2753ce5a1493a7962
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/24/2018
ms.locfileid: "47591629"
---
# <a name="ca2120-secure-serialization-constructors"></a>CA2120: serialization 생성자를 안전하게 하십시오.
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [CA2120: serialization 생성자를 보안](https://docs.microsoft.com/visualstudio/code-quality/ca2120-secure-serialization-constructors)합니다.

|||
|-|-|
|TypeName|SecureSerializationConstructors|
|CheckId|CA2120|
|범주|Microsoft.Security|
|변경 수준|주요 변경|

## <a name="cause"></a>원인
 형식에서 구현 된 <xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName> 인터페이스, 대리자 또는 인터페이스 아니며 부분적으로 신뢰할 수 있는 호출자를 허용 하는 어셈블리에서 선언 됩니다. 형식에 사용 하는 생성자는 <xref:System.Runtime.Serialization.SerializationInfo?displayProperty=fullName> 개체 및 <xref:System.Runtime.Serialization.StreamingContext?displayProperty=fullName> 개체 (serialization 생성자 서명). 이 생성자는 보안 검사를 통해 보안 되지 있지만 하나 이상의 정규 생성자 형식에 보안이 설정 됩니다.

## <a name="rule-description"></a>규칙 설명
 이 규칙은 사용자 지정 serialization을 지 원하는 형식에 적합 합니다. 형식을 구현 하는 경우 사용자 지정 serialization을 지원 합니다 <xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName> 인터페이스입니다. Serialization 생성자를 사용 하는 필수 항목이 며 역직렬화 할 시키거나 다시 사용 하 여 serialize 된 개체를 만드는 데 사용 되는 <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A?displayProperty=fullName> 메서드. Serialization 생성자를 할당 하 고 개체를 초기화, 때문에 일반 생성자에는 없는 보안 검사 serialization 생성자에 수도 있어야 합니다. 이 규칙을 위반 하면 그렇지 않은 경우 인스턴스를 만들지 못했습니다 호출자 이렇게 하려면 serialization 생성자를 사용할 수 있습니다.

## <a name="how-to-fix-violations"></a>위반 문제를 해결하는 방법
 이 규칙 위반 문제를 해결 하려면 다른 생성자를 보호 하는 동일한 보안 요청을 사용 하 여 serialization 생성자를 보호 합니다.

## <a name="when-to-suppress-warnings"></a>경고를 표시하지 않는 경우
 규칙의 위반을 표시 하지 마십시오.

## <a name="example"></a>예제
 다음 예제에서는 규칙을 위반 하는 형식을 보여 줍니다.

 [!code-csharp[FxCop.Security.SerialCtors#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Security.SerialCtors/cs/FxCop.Security.SerialCtors.cs#1)]

## <a name="related-rules"></a>관련된 규칙
 [CA2229: serialization 생성자를 구현하십시오.](../code-quality/ca2229-implement-serialization-constructors.md)

 [CA2237: ISerializable 형식을 SerializableAttribute로 표시하십시오.](../code-quality/ca2237-mark-iserializable-types-with-serializableattribute.md)

## <a name="see-also"></a>참고 항목
 <xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName> <xref:System.Runtime.Serialization.SerializationInfo?displayProperty=fullName>
 <xref:System.Runtime.Serialization.StreamingContext?displayProperty=fullName>


