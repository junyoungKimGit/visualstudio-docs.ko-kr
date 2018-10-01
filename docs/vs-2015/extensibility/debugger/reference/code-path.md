---
title: CODE_PATH | Microsoft Docs
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
- CODE_PATH
helpviewer_keywords:
- CODE_PATH structure
ms.assetid: 2d4b2890-4c9d-47e1-83c0-df9c6436427f
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 1f77ddf898732938f5a63c32ff26dd60e5a948e4
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47550903"
---
# <a name="codepath"></a>CODE_PATH
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [CODE_PATH](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/code-path)합니다.  
  
메서드 또는 함수 호출을 설명합니다.  
  
## <a name="syntax"></a>구문  
  
```cpp#  
typedef struct tagCODE_PATH {   
   BSTR                bstrName;  
   IDebugCodeContext2* pCode;  
} CODE_PATH;  
```  
  
```csharp  
public struct CODE_PATH {  
   public string            bstrName;  
   public IDebugCodeContext pCode;  
}  
```  
  
## <a name="members"></a>멤버  
 bstrName  
 코드 경로의 이름입니다.  
  
 pCode  
 합니다 [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) 함수 한 단계씩 코드에서 위치 식별 하는 개체입니다.  
  
## <a name="remarks"></a>설명  
 이 구조는 함수를 한 단계씩 실행 구현 됩니다. [EnumCodePaths](../../../extensibility/debugger/reference/idebugprogram2-enumcodepaths.md) 디버깅 중인 프로그램의 현재 위치에서 모든 호출을 반환 합니다. 이 구조는 이러한 한 번 호출을 나타냅니다.  
  
## <a name="requirements"></a>요구 사항  
 헤더: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>참고 항목  
 [구조체 및 공용 구조체](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)   
 [EnumCodePaths](../../../extensibility/debugger/reference/idebugprogram2-enumcodepaths.md)
