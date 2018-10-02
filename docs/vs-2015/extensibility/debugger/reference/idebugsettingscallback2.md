---
title: IDebugSettingsCallback2 | Microsoft Docs
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
- IDebugSettingsCallback2 interface
ms.assetid: 7e525d0b-7d7a-4d1c-8b78-e1398fa922f2
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 184cab04a4eaca2bf444bd31d6c97a3e6f0f7685
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47541719"
---
# <a name="idebugsettingscallback2"></a>IDebugSettingsCallback2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [IDebugSettingsCallback2](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugsettingscallback2)합니다.  
  
디버그 엔진 메트릭 설정을 읽을 수 원격으로 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
IDebugSettingsCallback2D : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>구현자 참고 사항  
 이 인터페이스는 세션 디버그 관리자의 이벤트 콜백에 의해 구현 되 고 디버그 엔진에서 사용 합니다. [D] Dbgmetric.lib 대신 로컬로 사용도 없습니다.  
  
## <a name="methods"></a>메서드  
 다음 표에서의 메서드를 보여 줍니다. `IDebugSettingsCallback2`합니다.  
  
|메서드|설명|  
|------------|-----------------|  
|[EnumEEs](../../../extensibility/debugger/reference/idebugsettingscallback2-enumees.md)|언어 및 공급 업체 식별자를 지정 된 사용 가능한 식 계산기를 열거 합니다.|  
|[GetEELocalObject](../../../extensibility/debugger/reference/idebugsettingscallback2-geteelocalobject.md)|메트릭이 지정 된 식 계산기 로컬 개체를 검색 합니다.|  
|[GetEEMetricDword](../../../extensibility/debugger/reference/idebugsettingscallback2-geteemetricdword.md)|식 계산기의 지정 된 메트릭을에 해당 하는 값을 검색 합니다.|  
|[GetEEMetricFile](../../../extensibility/debugger/reference/idebugsettingscallback2-geteemetricfile.md)|이름 또는 메트릭을 지정 된 식 계산기 메트릭 파일을 검색 합니다.|  
|[GetEEMetricGuid](../../../extensibility/debugger/reference/idebugsettingscallback2-geteemetricguid.md)|이름이 지정 된 식 계산기 메트릭에 대 한 고유 식별자를 검색 합니다.|  
|[GetEEMetricString](../../../extensibility/debugger/reference/idebugsettingscallback2-geteemetricstring.md)|해당 이름이 지정 하는 식 계산기 메트릭의 값 문자열을 검색 합니다.|  
|[GetMetricDword](../../../extensibility/debugger/reference/idebugsettingscallback2-getmetricdword.md)|이름이 지정 된 메트릭 값을 검색 합니다.|  
|[GetMetricGuid](../../../extensibility/debugger/reference/idebugsettingscallback2-getmetricguid.md)|이름이 지정 된 메트릭의 고유 식별자를 검색 합니다.|  
|[GetMetricString](../../../extensibility/debugger/reference/idebugsettingscallback2-getmetricstring.md)|이름이 지정 된 메트릭 값 문자열을 검색 합니다.|  
  
## <a name="requirements"></a>요구 사항  
 헤더: Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="example"></a>예제  
 다음 예제에서는 사용 하는 함수는 **IDebugSettingsCallback2** 개체를 매개 변수로 합니다.  
  
```cpp#  
HRESULT GetDebugSettingsCallback (IDebugSettingsCallback2 **ppCallback)  
{  
    HRESULT hRes = E_FAIL;  
  
    if ( ppCallback )  
   {  
        if ( EVAL(m_pdec) )  
            hRes = m_pdec->QueryInterface(IID_IDebugSettingsCallback2, (void **)ppCallback);  
        else  
            hRes = E_FAIL;  
    }  
    else  
        hRes = E_INVALIDARG;  
  
    return ( hRes );  
}  
```
