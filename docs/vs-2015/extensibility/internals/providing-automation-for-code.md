---
title: 코드에 대 한 자동화 제공 | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- CodeModel object
ms.assetid: 21cb3e63-f25c-404b-bc1d-a32ad0fdd4d5
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 456927337331c15b3392b03175d83f2a63f87e77
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47541347"
---
# <a name="providing-automation-for-code"></a>코드에 대한 자동화 제공
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [코드에 대 한 자동화 제공](https://docs.microsoft.com/visualstudio/extensibility/internals/providing-automation-for-code)합니다.  
  
코드에 대 한 자동화 모델을 만들 필요는 없습니다. 환경 SDK는 이렇게 하는 것에 대 한 샘플을 제공 하지 않습니다. 코드 모델에 대 한 정보를 참조 하세요.를 <xref:EnvDTE.CodeModel> 개체입니다.  
  
 코드 모델을 구현 하려면 내부 데이터 구조에 의해 결정 되는 모든 인터페이스를 구현 해야 합니다. 개체에서 파생 되어야 합니다는 `IDispatch` 클래스입니다.  
  
 를 확장 하는 개체 <xref:EnvDTE.CodeModel> 하 고 <xref:EnvDTE.FileCodeModel>에서 사용할 수는 <xref:EnvDTE.Project> 개체를 다음과 같이 표시:  
  
 <xref:EnvDTE.Project.CodeModel%2A>  
  
 <xref:EnvDTE.ProjectItem.FileCodeModel%2A>  
  
 구현 하도록 선택할 수 있습니다만 `CodeModel` 또는 `FileCodeModel` 에서 반환 된 개체의 인터페이스에 `Project` 및 <xref:EnvDTE.ProjectItem> 개체입니다. 프로젝트 시스템에 대 한 적절 한이 인터페이스에서 모든 기능을 제공 합니다.  
  
 메서드 또는 속성을 같은 기능을 추가 하려는 경우 사용할 수 없는 표준에서 `CodeModel` 고 `FileCodeModel` 인터페이스를 표준에서 상속 되는 고유한 인터페이스를 만듭니다. 최종 사용자는 쉽게 알 수 있도록 프로젝트 시스템을 사용 하 여 문서를 사용 해야 합니다. 표준 인터페이스를 반환 하지만 사용자를 호출할 수는 `QueryInterface` 메서드나 인터페이스 존재 알려져 있는 경우로 캐스팅 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [자동화 모델 개요](../../extensibility/internals/automation-model-overview.md)
