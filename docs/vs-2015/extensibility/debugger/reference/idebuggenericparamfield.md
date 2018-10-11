---
title: IDebugGenericParamField | Microsoft Docs
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
- IDebugGenericParamField interface
ms.assetid: ba24f499-5ba7-4c67-83e6-923229b52327
caps.latest.revision: 7
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 841331b496aa21687a7ebdf90a6f4eee40b5ae89
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47551931"
---
# <a name="idebuggenericparamfield"></a>IDebugGenericParamField
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [IDebugGenericParamField](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebuggenericparamfield)합니다.  
  
관리 코드 제네릭 형식에 대 한 매개 변수를 나타냅니다.  
  
## <a name="syntax"></a>구문  
  
```  
IDebugGenericParamField : IDebugField  
```  
  
## <a name="notes-for-implementers"></a>구현자 참고 사항  
 제네릭의 지원에 사용 됩니다.  
  
## <a name="methods"></a>메서드  
 메서드 외에도 합니다 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) 인터페이스에서이 인터페이스는 다음 메서드를 구현 합니다.  
  
|메서드|설명|  
|------------|-----------------|  
|[ConstraintCount](../../../extensibility/debugger/reference/idebuggenericparamfield-constraintcount.md)|이 제네릭 매개 변수를 사용 하 여 연결 된 제약 조건의 수를 반환 합니다.|  
|[GetConstraints](../../../extensibility/debugger/reference/idebuggenericparamfield-getconstraints.md)|이 제네릭 매개 변수를 사용 하 여 연결 된 제약 조건을 검색 합니다.|  
|[GetFlags](../../../extensibility/debugger/reference/idebuggenericparamfield-getflags.md)|이 제네릭 매개 변수에 대 한 플래그를 검색 합니다.|  
|[GetIndex](../../../extensibility/debugger/reference/idebuggenericparamfield-getindex.md)|이 제네릭 매개 변수의 인덱스를 검색합니다.|  
|[GetNameOfFormalParam](../../../extensibility/debugger/reference/idebuggenericparamfield-getnameofformalparam.md)|이 제네릭 매개 변수의 이름을 검색합니다.|  
|[GetOwner](../../../extensibility/debugger/reference/idebuggenericparamfield-getowner.md)|이 제네릭 매개 변수의 형식 또는 메서드의 소유자를 검색합니다.|  
  
## <a name="requirements"></a>요구 사항  
 헤더: Sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll
