---
title: IDiaInjectedSource::get_source | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaInjectedSource::get_source method
ms.assetid: 3c0b5386-321f-4f8f-85cc-e2ee7b4cc3d2
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b389df8220766ffbdbf865a2b8e70877fe91b3f1
ms.sourcegitcommit: 5f6ad1cefbcd3d531ce587ad30e684684f4c4d44
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/22/2019
ms.locfileid: "72743332"
---
# <a name="idiainjectedsourceget_source"></a>IDiaInjectedSource::get_source
소스 코드 바이트를 검색 합니다.

## <a name="syntax"></a>구문

```C++
HRESULT get_source ( 
   DWORD  cbData,
   DWORD* pcbData,
   BYTE   data[]
);
```

#### <a name="parameters"></a>매개 변수
 `cbData`

진행 데이터 버퍼의 크기를 나타내는 바이트 수입니다.

 `pcbData`

제한이 반환 된 바이트 수를 나타내는 바이트 수를 반환 합니다. @No__t_0 `pcbData` `NULL` 이면 사용할 수 있는 데이터의 총 바이트 수입니다.

 `data[]`

제한이 원본 바이트로 채워질 버퍼입니다.

## <a name="return-value"></a>반환 값
 성공하면 `S_OK`를 반환합니다. 이 속성이 지원 되지 않는 경우 `S_FALSE`를 반환 합니다. 그러지 않으면 오류 코드가 반환됩니다.

## <a name="see-also"></a>참조
- [IDiaInjectedSource](../../debugger/debug-interface-access/idiainjectedsource.md)