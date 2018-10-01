---
title: 'CA1412: ComSource 인터페이스 표시 IDispatch로 | Microsoft Docs'
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
- MarkComSourceInterfacesAsIDispatch
- CA1412
helpviewer_keywords:
- CA1412
- MarkComSourceInterfacesAsIDispatch
ms.assetid: 131a7563-0410-443c-a8f5-52104250cfb4
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 18404cf19c8ecb1554dcd14914128130ec36e366
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/24/2018
ms.locfileid: "47591569"
---
# <a name="ca1412-mark-comsource-interfaces-as-idispatch"></a>CA1412: ComSource 인터페이스를 IDispatch로 표시하십시오.
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [CA1412: IDispatch로 표시 ComSource 인터페이스](https://docs.microsoft.com/visualstudio/code-quality/ca1412-mark-comsource-interfaces-as-idispatch)합니다.

|||
|-|-|
|TypeName|MarkComSourceInterfacesAsIDispatch|
|CheckId|CA1412|
|범주|Microsoft.Interoperability|
|변경 수준|주요 변경|

## <a name="cause"></a>원인
 형식으로 표시 됩니다는 <xref:System.Runtime.InteropServices.ComSourceInterfacesAttribute> 특성 및 하나 이상의 지정 된 인터페이스로 표시 되지 합니다 <xref:System.Runtime.InteropServices.InterfaceTypeAttribute> 특성이로 설정 합니다 `InterfaceIsDispatch` 값.

## <a name="rule-description"></a>규칙 설명
 <xref:System.Runtime.InteropServices.ComSourceInterfacesAttribute> 구성 요소 개체 모델 (COM) 클라이언트에 클래스 노출 하는 이벤트 인터페이스를 식별 하는 데 사용 됩니다. 이러한 인터페이스를 노출 해야 `InterfaceIsIDispatch` Visual Basic 6 COM 클라이언트에서 이벤트 알림을 받을 수 있도록 합니다. 인터페이스를 사용 하 여 표시 되지 않으면 기본적으로는 <xref:System.Runtime.InteropServices.InterfaceTypeAttribute> 특성 이중 인터페이스로 노출 됩니다.

## <a name="how-to-fix-violations"></a>위반 문제를 해결하는 방법
 이 규칙 위반 문제를 해결 하려면 추가 하거나 수정 합니다 <xref:System.Runtime.InteropServices.InterfaceTypeAttribute> InterfaceIsIDispatch를 사용 하 여 지정 된 모든 인터페이스에 대 한 해당 값이 설정 되도록 특성의 <xref:System.Runtime.InteropServices.ComSourceInterfacesAttribute> 특성입니다.

## <a name="when-to-suppress-warnings"></a>경고를 표시하지 않는 경우
 이 규칙에서는 경고를 표시해야 합니다.

## <a name="example"></a>예제
 다음 예제에서는 규칙을 위반 하는 인터페이스 중 하나는 클래스를 보여 줍니다.

 [!code-csharp[FxCop.Interoperability.MarkIDispatch#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Interoperability.MarkIDispatch/cs/FxCop.Interoperability.MarkIDispatch.cs#1)]
 [!code-vb[FxCop.Interoperability.MarkIDispatch#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Interoperability.MarkIDispatch/vb/FxCop.Interoperability.MarkIDispatch.vb#1)]

## <a name="related-rules"></a>관련된 규칙
 [CA1408: AutoDual ClassInterfaceType을 사용하지 마십시오.](../code-quality/ca1408-do-not-use-autodual-classinterfacetype.md)

## <a name="see-also"></a>참고 항목
 [방법: COM 싱크에서 처리 하는 이벤트를 발생 시킬](http://msdn.microsoft.com/en-us/7c9944b2-e951-4c3e-a0a1-59b2ae37d7fd) [비관리 코드와의 상호 운용](http://msdn.microsoft.com/library/ccb68ce7-b0e9-4ffb-839d-03b1cd2c1258)


