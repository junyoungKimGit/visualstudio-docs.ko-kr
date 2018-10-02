---
title: UML 모델 요소에 참조 문자열 연결 | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- UML - extending, reference strings
ms.assetid: 15dbed99-efce-42fe-a768-714a5804e7d1
caps.latest.revision: 11
author: alexhomer1
ms.author: gewarren
manager: douge
ms.openlocfilehash: 0d917bf0553fbea06c73d3f4ce57f01b3f99a36d
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47543869"
---
# <a name="attach-reference-strings-to-uml-model-elements"></a>UML 모델 요소에 참조 문자열 연결
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [UML에 참조 문자열 연결 모델 요소](https://docs.microsoft.com/visualstudio/modeling/attach-reference-strings-to-uml-model-elements)합니다.  
  
모델 요소에 임의 문자열을 연결하는 코드를 작성할 수 있습니다. 예를 들어 문자열은 URI, 캐시된 계산 결과 또는 다른 모델의 요소에 대한 ModelBus 참조일 수 있습니다. 각 문자열은 IReference 개체에 포함됩니다. 개수에 관계없이 IReference 개체를 각 모델 요소에 연결할 수 있습니다.  
  
 각 IReference 개체에는 이름이 있습니다. 이 이름을 사용하여 참조 값을 해석하는 방법을 나타낼 수 있습니다. 예를 들어 이름을 "URI"로 설정하여 값이 URI로 해석되어야 함을 나타낼 수 있습니다. 모델링 도구에서 사용하는 몇 가지 미리 정의된 참조 이름 값이 있습니다.  
  
## <a name="attaching-a-reference-to-an-ielement"></a>IElement에 참조 연결  
 다음 메서드를 사용하려면 아래 항목에 대한 참조를 추가해야 합니다.  
  
 Microsoft.VisualStudio.ArchitectureTools.Extensibility.dll  
  
 코드에 다음 지시어를 삽입해야 합니다.  
  
 `using Microsoft.VisualStudio.ArchitectureTools.Extensibility.Uml;`  
  
|메서드 호출|설명|  
|-----------------|-----------------|  
|`element.AddReference (nameString, valueString, duplicatesAllowed)`|지정된 이름 및 값 문자열을 사용하여 `IReference`를 만들고 `element`에 연결합니다. `IReference`를 반환합니다.<br /><br /> `duplicatesAllowed`가 false이고 동일한 이름을 가진 `IReference`가 이미 `element`에 연결되어 있으면 예외가 발생합니다.|  
|`element.GetReferences(name)`|지정된 `IReference`을 가진, `element`에 연결된 `name` 개체를 모두 반환합니다.|  
|`element.DeleteAllReferences(name)`|지정된 이름을 가진, 요소에 연결된 `IReference` 개체를 모두 삭제합니다.|  
|`reference.Delete()`|이 `IReference`를 삭제합니다.|  
|`ReferenceConstants.WorkItem`|작업 항목 참조에 이름을 지정하는 데 사용되는 값입니다.|  
  
## <a name="see-also"></a>참고 항목  
 [작업 항목 링크 처리기 정의](../modeling/define-a-work-item-link-handler.md)   
 [모델링 확장 정의 및 설치](../modeling/define-and-install-a-modeling-extension.md)   
 [UML API를 사용한 프로그래밍](../modeling/programming-with-the-uml-api.md)


