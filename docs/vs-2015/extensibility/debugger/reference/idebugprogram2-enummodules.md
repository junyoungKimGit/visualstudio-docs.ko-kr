---
title: IDebugProgram2::EnumModules | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugProgram2::EnumModules
helpviewer_keywords:
- IDebugProgram2::EnumModules
ms.assetid: 876ac9da-3b7c-4156-b79a-8f340e9fcea6
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: ef011a0e408fbe32b1bf35c962e65fd54f60a78b
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47553544"
---
# <a name="idebugprogram2enummodules"></a>IDebugProgram2::EnumModules
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [IDebugProgram2::EnumModules](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugprogram2-enummodules)합니다.  
  
이 프로그램에 로드 하 고 실행 되는 모듈의 목록을 검색 합니다.  
  
## <a name="syntax"></a>구문  
  
```cpp#  
HRESULT EnumModules(   
   IEnumDebugModules2** ppEnum  
);  
```  
  
```csharp  
int EnumModules(   
   out IEnumDebugModules2 ppEnum  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `ppEnum`  
 [out] 반환 된 [IEnumDebugModules2](../../../extensibility/debugger/reference/ienumdebugmodules2.md) 모듈의 목록을 포함 하는 개체입니다.  
  
## <a name="return-value"></a>반환 값  
 성공 하면 반환 `S_OK`고, 그렇지 않으면 오류 코드를 반환 합니다.  
  
## <a name="remarks"></a>설명  
 모듈 DLL 또는 어셈블리 이며 일반적으로 나오는 합니다 **모듈** 디버그 창입니다.  
  
## <a name="see-also"></a>참고 항목  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [IEnumDebugModules2](../../../extensibility/debugger/reference/ienumdebugmodules2.md)
