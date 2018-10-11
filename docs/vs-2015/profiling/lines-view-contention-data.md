---
title: 줄 뷰 - 경합 데이터 | Microsoft 문서
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Lines view
ms.assetid: 859b02d2-eddf-4ad3-95de-0df67ee2ab03
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 09149f44e80155a13986d42d2b3279e5c39c8884
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47552719"
---
# <a name="lines-view---contention-data"></a>줄 뷰 - 경합 데이터
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [줄 뷰-경합 데이터](https://docs.microsoft.com/visualstudio/profiling/lines-view-contention-data)입니다.  
  
경합 데이터의 줄 뷰에는 프로파일링 실행 시 샘플이 수집될 때 실행되고 있던 문에 대한 성능 데이터가 나열됩니다. 소스 파일에서는 하나의 문이 소스 파일의 여러 줄에 걸쳐 있거나 한 줄에 여러 문이 포함될 수 있습니다.  
  
 문은 다음 데이터에 의해 식별됩니다.  
  
-   함수 문이 포함된 소스 파일.  
  
-   문이 포함된 함수.  
  
-   문이 시작되는 소스 줄.  
  
-   문이 시작되는 소스 줄의 문자.  
  
-   문이 끝나는 소스 줄.  
  
-   문이 끝나는 소스 줄의 문자.  
  
 줄 이름 열은 식별자 데이터의 정렬 가능한 연결을 제공합니다.  
  
 다음 표에서는 줄 뷰 보고서의 열에 대해 설명합니다.  
  
|열|설명|  
|------------|-----------------|  
|**차단된 전용 시간**|경합 이벤트로 인해 문의 코드를 실행할 수 없도록 이 문이 차단된 시간입니다. 문이 호출한 함수의 차단된 시간은 포함되지 않습니다.|  
|**차단된 전용 시간 비율(%)**|프로세스에서 문의 차단된 전용 시간이었던 모든 차단된 시간의 백분율입니다.|  
|**전용 경합**|경합 이벤트로 인해 문의 코드를 실행할 수 없도록 이 문이 차단된 횟수입니다. 문이 호출한 함수의 경합 이벤트는 포함되지 않습니다.|  
|**전용 경합 비율(%)**|프로세스에서 이 문의 전용 경합이었던 모든 경합 이벤트의 백분율입니다.|  
|**함수 주소**|이 문을 포함하는 함수의 주소입니다.|  
|**함수 이름**|이 문을 포함하는 함수의 정규화된 이름입니다.|  
|**차단된 포괄 시간**|이 문과 문에서 호출된 함수에서 차단된 시간입니다.|  
|**차단된 포괄 시간 비율(%)**|프로세스에서 문의 차단된 포괄 시간이었던 모든 차단된 시간의 백분율입니다.|  
|**포괄 경합**|이 문과 해당 문에서 호출된 함수가 실행할 수 없도록 차단된 횟수입니다.|  
|**포괄 경합 비율(%)**|프로세스에서 이 문의 포괄 경합이었던 모든 경합 이벤트의 백분율입니다.|  
|**줄 이름**|프로파일러에서 생성된 줄 식별자입니다. 이 식별자에는 다음 구문이 사용됩니다. `SourceFile`**;[**`LineNumberStart`**,**`CharacterStart`**]->;[**`LineNumberEnd`**,**`CharacterEnd`**]**|  
|**함수 줄 번호**|소스 파일에서 이 함수가 시작되는 줄 번호입니다.|  
|**모듈 이름**|문이 포함된 모듈의 이름입니다.|  
|**모듈 경로**|문이 포함된 모듈의 경로입니다.|  
|**프로세스 ID**|프로파일링된 프로세스의 PID(프로세스 ID)입니다.|  
|**프로세스 이름**|프로세스의 이름입니다.|  
|**소스 문자 시작**|이 문이 시작되는 소스 파일 줄에서 시작 문자의 오프셋입니다.|  
|**소스 문자 끝**|이 문이 끝나는 소스 파일 줄에서 시작 문자의 오프셋입니다.|  
|**소스 파일**|함수 문이 포함된 소스 파일의 이름입니다.|  
|**소스 줄 시작**|문이 시작되는 소스 파일의 줄 번호입니다.|  
|**소스 줄 끝**|문이 끝나는 소스 파일의 줄 번호입니다.|  
  
## <a name="see-also"></a>참고 항목  
 [방법: 보고서 뷰 열 사용자 지정](../profiling/how-to-customize-report-view-columns.md)   
 [줄 뷰](../profiling/lines-view.md)   
 [줄 뷰 - 샘플링](../profiling/lines-view-dotnet-memory-sampling-data.md)   
 [줄 뷰](../profiling/lines-view-sampling-data.md)


