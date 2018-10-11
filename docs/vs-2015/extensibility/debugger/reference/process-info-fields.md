---
title: PROCESS_INFO_FIELDS | Microsoft Docs
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
- PROCESS_INFO_FIELDS
helpviewer_keywords:
- PROCESS_INFO_FIELDS enumeration
ms.assetid: 0d9cc345-3d3a-44d8-ae15-a67acb97a828
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 8b272fba2e05c25e60b2db1f11be16b97d261101
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47554870"
---
# <a name="processinfofields"></a>PROCESS_INFO_FIELDS
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [PROCESS_INFO_FIELDS](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/process-info-fields)합니다.  
  
프로세스에 대 한 검색할 정보의 종류를 지정 합니다.  
  
## <a name="syntax"></a>구문  
  
```cpp#  
enum enum_PROCESS_INFO_FIELDS {   
   PIF_FILE_NAME             = 0x00000001,  
   PIF_BASE_NAME             = 0x00000002,  
   PIF_TITLE                 = 0x00000004,  
   PIF_PROCESS_ID            = 0x00000008,  
   PIF_SESSION_ID            = 0x00000010,  
   PIF_ATTACHED_SESSION_NAME = 0x00000020,  
   PIF_CREATION_TIME         = 0x00000040,  
   PIF_FLAGS                 = 0x00000080,  
   PIF_ALL                   = 0x000000ff  
};  
typedef DWORD PROCESS_INFO_FIELDS;  
```  
  
```csharp  
public enum enum_PROCESS_INFO_FIELDS {   
   PIF_FILE_NAME             = 0x00000001,  
   PIF_BASE_NAME             = 0x00000002,  
   PIF_TITLE                 = 0x00000004,  
   PIF_PROCESS_ID            = 0x00000008,  
   PIF_SESSION_ID            = 0x00000010,  
   PIF_ATTACHED_SESSION_NAME = 0x00000020,  
   PIF_CREATION_TIME         = 0x00000040,  
   PIF_FLAGS                 = 0x00000080,  
   PIF_ALL                   = 0x000000ff  
};  
```  
  
## <a name="members"></a>멤버  
 PIF_FILE_NAME  
 초기화/사용 된 `bstrFileName` 필드를 [PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md) 구조입니다.  
  
 PIF_BASE_NAME  
 초기화/사용 된 `bstrBaseName` 필드는 `PROCESS_INFO` 구조입니다.  
  
 PIF_TITLE  
 초기화/사용 된 `bstrTitle` 필드는 `PROCESS_INFO` 구조입니다.  
  
 PIF_PROCESS_ID  
 초기화/사용 된 `ProcessId` 필드는 `PROCESS_INFO` 구조입니다.  
  
 PIF_SESSION_ID  
 초기화/사용 된 `dwSessionId` 필드는 `PROCESS_INFO` 구조입니다.  
  
 PIF_ATTACHED_SESSION_NAME  
 초기화/사용 된 `bstrAttachedSessionName` 필드는 `PROCESS_INFO` 구조입니다.  
  
 PIF_CREATION_TIME  
 초기화/사용 된 `CreationTime` 필드는 `PROCESS_INFO` 구조입니다.  
  
 PIF_FLAGS  
 초기화/사용 된 `Flags` 필드는 `PROCESS_INFO` 구조입니다.  
  
 PIF_ALL  
 모든 필드를 채웁니다.  
  
## <a name="remarks"></a>설명  
 에 전달 합니다 [GetInfo](../../../extensibility/debugger/reference/idebugprocess2-getinfo.md) 의 필드를 표시 하는 방법을 [PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md) 구조는 초기화할 합니다.  
  
 에서도 사용 됩니다 `Fields` 필드는 `PROCESS_INFO` 에 유효 하 고 사용 되는 필드는 구조체.  
  
 이러한 플래그는 비트과 결합 될 수 `OR`입니다.  
  
## <a name="requirements"></a>요구 사항  
 헤더: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>참고 항목  
 [열거형](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md)
