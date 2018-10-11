---
title: TargetPlatformName 요소 (Visual Studio 템플릿) | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 3a6b1f45-b5d6-418e-add1-87ee8f15033d
caps.latest.revision: 6
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 4a82a30c8df696e5666d81b18a8f60641debf828
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47553245"
---
# <a name="targetplatformname-element-visual-studio-templates"></a>TargetPlatformName 요소(Visual Studio 템플릿)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [TargetPlatformName 요소 (Visual Studio 템플릿)](https://docs.microsoft.com/visualstudio/extensibility/targetplatformname-element-visual-studio-templates)합니다.  
  
프로젝트 템플릿의 대상 플랫폼을 지정합니다. 이 요소는 프로젝트 템플릿을 만들려면 사용 되도록 지정 데 [!INCLUDE[win8_appname_long](../includes/win8-appname-long-md.md)] 앱.  
  
## <a name="syntax"></a>구문  
  
```xml  
<VSTemplate>  
    <TemplateData>   
        <TargetPlatformName> OperatingSystem</TargetPlatformName>  
```  
  
## <a name="attributes-and-elements"></a>특성 및 요소  
 다음 섹션에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.  
  
### <a name="attributes"></a>특성  
 없음  
  
### <a name="child-elements"></a>자식 요소  
  
|요소|설명|  
|-------------|-----------------|  
|[RequiredPlatformVersion](../extensibility/requiredplatformversion-element-visual-studio-templates.md)|프로젝트 템플릿의 대상 운영 체제 버전을 지정합니다.|  
  
### <a name="parent-elements"></a>부모 요소  
  
|요소|설명|  
|-------------|-----------------|  
|[TemplateData](../extensibility/templatedata-element-visual-studio-templates.md)|템플릿을 분류하고 **새 프로젝트** 또는 **새 항목 추가** 대화 상자에서 템플릿이 표시되는 방식을 정의합니다.|  
  
## <a name="text-value"></a>텍스트 값  
 텍스트 값은 필수입니다.  
  
## <a name="remarks"></a>설명  
 텍스트는 **Windows**여야 합니다.  
  
## <a name="example"></a>예제  
 이 예제에서는 지정 하는 프로젝트 템플릿의 대상 [!INCLUDE[win8](../includes/win8-md.md)] 이상.  
  
```xml  
<VSTemplate Type="Project" Version="3.0.0" xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">   
    <TemplateData>   
        <TargetPlatformName>Windows</TargetPlatformName>   
        <RequiredPlatformVersion>8</RequiredPlatformVersion>   
    </TemplateData>   
    <TemplateContent> </TemplateContent>  
</VSTemplate>  
```  
  
## <a name="see-also"></a>참고 항목  
 [프로젝트 템플릿 및 항목 템플릿 만들기](../ide/creating-project-and-item-templates.md)   
 [Visual Studio 템플릿 스키마 참조](../extensibility/visual-studio-template-schema-reference.md)
