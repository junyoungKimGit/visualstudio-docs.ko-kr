---
title: 상수 (Debug Interface Access SDK) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- constants, DIA SDK
- DIA SDK, constants
ms.assetid: aca4ec77-bc08-4cdd-a6ce-8d4a28ea5ea3
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b10ab87f056bc153ec41c125b0e01ddefa139b80
ms.sourcegitcommit: 5f6ad1cefbcd3d531ce587ad30e684684f4c4d44
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/22/2019
ms.locfileid: "72745407"
---
# <a name="constants-debug-interface-access-sdk"></a>상수(디버그 인터페이스 액세스 SDK)
이러한 문자열 상수를 사용 하 여 DIA SDK를 통해 PDB (프로그램 디버그 데이터베이스) 파일의 다양 한 섹션을 식별할 수 있습니다.

## <a name="constants"></a>상수
다음은 C/C++ 매크로로 선언 됩니다.

|매크로|값|
|-----------|-----------|
|`DiaTable_Symbols`|L "기호"|
|`DiaTable_Sections`|L "섹션"|
|`DiaTable_SrcFiles`|L "SourceFiles"|
|`DiaTable_LineNums`|L "LineNumbers"|
|`DiaTable_SegMap`|L "SegmentMap"|
|`DiaTable_Dbg`|L "Dbg"|
|`DiaTable_InjSrc`|L "InjectedSource"|
|`DiaTable_FrameData`|L "FrameData"|

## <a name="example"></a>예제
다음은 이러한 기호 중 하나를 사용 하는 예제입니다.

```C++
HRESULT GetSymbolTable(IDiaEnumTables *pEnumTables, IDiaTable **pTable)
{
    HRESULT hr;
    VARIANT var;
    var.vt      = VT_BSTR;
    var.bstrVal = SysAllocString( DiaTable_Symbols );
    hr = pEnumTables->Item( var, pTable );
    return(hr);
}
```

## <a name="requirements"></a>요구 사항
헤더: dia2

## <a name="see-also"></a>참조
- [참조](../../debugger/debug-interface-access/debug-interface-access-sdk-reference.md)
- [열거형 및 구조체](../../debugger/debug-interface-access/enumerations-and-structures.md)
- [인터페이스(디버그 인터페이스 액세스 SDK)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)
- [IDiaEnumTables::Item](../../debugger/debug-interface-access/idiaenumtables-item.md)
