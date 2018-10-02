---
title: UML 동작 다이어그램 요소의 속성 | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.teamarch.activitydiagram.shapes.properties
helpviewer_keywords:
- UML, element properties
- activity diagrams, properties
ms.assetid: 9849d45e-65d5-46bd-a319-757e90b7c748
caps.latest.revision: 19
author: alexhomer1
ms.author: gewarren
manager: douge
ms.openlocfilehash: c50a84f9e3c5425459ea458c3f6bbc282d64b0b1
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47542679"
---
# <a name="properties-of-elements-on-uml-activity-diagrams"></a>UML 동작 다이어그램 요소의 속성
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [UML 동작 다이어그램 요소의 속성](https://docs.microsoft.com/visualstudio/modeling/properties-of-elements-on-uml-activity-diagrams)합니다.  
  
UML 동작 다이어그램에서 다이어그램의 각 요소에는 속성이 있습니다. 요소의 속성을 보려면 다이어그램 또는 요소를 마우스 오른쪽 단추로 **UML 모델 탐색기** 을 클릭 한 다음 **속성**합니다. 속성에 표시 된 **속성** 창입니다.  
  
> [!NOTE]
>  이 항목은 UML 동작 다이어그램 요소의 속성에 대한 것입니다. UML 동작 다이어그램을 읽는 방법에 대 한 자세한 내용은 [UML 동작 다이어그램: 참조](../modeling/uml-activity-diagrams-reference.md)합니다. UML 동작 다이어그램을 그리는 방법에 대 한 자세한 내용은 참조 하세요. [UML 동작 다이어그램: 지침](../modeling/uml-activity-diagrams-guidelines.md)합니다.  
  
## <a name="properties-of-elements"></a>요소의 속성  
  
|속성|기본값|요소|설명|  
|--------------|-------------|-------------|-----------------|  
|**이름**|기본 이름|모두|요소를 식별합니다.|  
|**정규화 된 이름**|패키지 :: 이름|모두|요소를 고유하게 식별합니다. 요소를 포함하는 패키지의 정규화된 이름이 접두사로 추가됩니다.|  
|**작업 항목**|0 associated|모두|이 요소와 연결된 작업 항목 수입니다. 작업 항목에 연결 하려면을 참조 하세요 [모델 요소에 연결 하 고 작업 항목](../modeling/link-model-elements-and-work-items.md)합니다.|  
|**설명**|(없음)|모두|여기서 요소에 대한 일반적인 메모를 만들 수 있습니다.|  
|**색**|(형식 기본값)|모두|도형의 색입니다.|  
|**본문**|(없음)|작업|작업을 자세히 지정합니다.|  
|**언어**|(없음)|작업|본문에 있는 식의 언어입니다.|  
|**로컬 사후 조건**|(없음)|작업, 보내기, 수락, 호출 동작, 호출 작업|실행 종료 시 충족되어야 하는 제약 조건입니다. 작업을 통해 달성되는 목표입니다.|  
|**로컬 사전 조건**|(없음)|작업, 보내기, 수락, 호출 동작, 호출 작업|실행 시작 전에 충족되어야 하는 제약 조건입니다.|  
|**동기적인**|True|호출 동작, 호출 작업|-True 이면 동작이 종료 될 때까지 작업이 대기 합니다.|  
|**동작**|(없음)|호출 동작|-호출 된 동작입니다.|  
|**작업**|(없음)|호출 작업|-호출 작업입니다.|  
|**역 마샬링**|False|수락 이벤트|-True 이면 여러 개의 형식화 된 출력 핀 있을 수 있으며 데이터가 늘어나면 마샬링된 합니다. False이면 모든 데이터가 한 핀에 나타납니다.|  
|**상한**|**\***|개체 노드, 동작 매개 변수|**0** 데이터 흐름을 따라 직접 전달 해야 한다는 의미입니다.<br /><br /> **\*** 흐름에서 데이터를 저장할 수 있다는 것을 나타냅니다.|  
|**선택**|(없음)|개체 노드, 동작 매개 변수, 입력 핀, 출력 핀, 개체 흐름|데이터를 필터링하는 프로세스를 호출합니다. 이 프로세스는 다른 다이어그램에서 정의될 수 있습니다.|  
|**정렬**|(없음)|개체 노드, 동작 매개 변수, 입력 핀, 출력 핀|-여러 토큰이 저장 됩니다.|  
|**컨트롤**|False|입력 핀, 출력 핀|-True 이면이 핀의 흐름이 제어 흐름이입니다. false이면 개체 흐름입니다.|  
|**Type**|(없음)|입력 핀, 출력 핀, 개체 노드, 동작 매개 변수|-전송 되는 개체의 형식입니다.<br />-형식은 Integer와 같은 기본 형식이 될 수 또는 분류자를 모델의 다른 곳에서 정의 합니다. 정의 되지 않은 형식의 이름을 입력 하면 경우에 표시 됩니다는 **지정 되지 않은 형식** UML 모델 탐색기의 섹션입니다.|  
|**다중성**|1|입력 핀, 출력 핀|-단일 값 또는 범위 수 있습니다 `[n..m]`합니다.<br />-하한값 `n` -작업 수 없습니다 (입력된 핀)에 대 한 시작 또는 중지 (출력 핀) 때까지 `n` 핀 대기 하는 개체입니다.<br />-상한 `m` -작업을 사용 하거나 생성 없습니다 둘 `m` 한 번 실행에서 하는 개체입니다. *는 무제한을 의미합니다.|  
|**변환**|(없음)|개체 흐름|-데이터를 변환 하는 프로세스를 호출 합니다. 이 프로세스는 다른 다이어그램에서 정의될 수 있습니다.|  
|**멀티 캐스트**|False|개체 흐름|-있을 수 있음을 여러 받는 사람 개체 또는 구성 요소를 나타냅니다.|  
|**다중 수신**|False|개체 흐름|-있을 수 있음을 여러 받는 사람 개체 또는 구성 요소를 나타냅니다.|  
|**단일 실행**|False|활동 다이어그램|-는 최대 한 번에 하나의 실행이 다이어그램을 설정 합니다.|  
  
## <a name="see-also"></a>참고 항목  
 [UML 동작 다이어그램: 참조](../modeling/uml-activity-diagrams-reference.md)   
 [UML 동작 다이어그램: 지침](../modeling/uml-activity-diagrams-guidelines.md)


