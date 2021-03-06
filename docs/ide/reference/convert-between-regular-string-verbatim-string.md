---
title: 일반 문자열 리터럴과 축자 문자열 리터럴 간 변환
description: 빠른 작업 및 리팩터링 메뉴를 사용하여 일반 문자열과 축자 문자열 리터럴 간에 변환하는 방법을 알아봅니다.
ms.custom: SEO-VS-2020
ms.date: 06/08/2020
ms.topic: reference
author: mikadumont
ms.author: midumont
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: d50b979902e6eb5a606305b262f5009caef87467
ms.sourcegitcommit: 967c2f8c1b3f805cf42c0246389517689d971b53
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/25/2020
ms.locfileid: "96040461"
---
# <a name="convert-between-regular-string-and-verbatim-string-literals-refactoring"></a>일반 문자열 리터럴과 축자 문자열 리터럴 간 변환 리팩터링

이 리팩터링은 다음에 적용됩니다.

- C#

**내용:** 일반 문자열 리터럴과 축자 문자열 리터럴 간에 변환할 수 있습니다.

**시기:** 코드에서 공간을 절약하거나 코드를 더 명확하게 만들려고 합니다.

**이유:** 축자 문자열 리터럴을 일반 문자열 리터럴로 변환하면 공간을 절약하는 데 도움이 될 수 있습니다. 일반 문자열 리터럴을 축자 문자열 리터럴로 변환하면 더 명확하게 파악할 수 있습니다.

## <a name="how-to"></a>방법

1. 일반 문자열 리터럴 또는 축자 문자열 리터럴에 캐럿을 추가합니다.

2. 줄의 임의 위치에서 **Ctrl**+ **.** 를 눌러 **빠른 작업 및 리팩터링** 메뉴를 트리거합니다.

3. 다음 옵션 중 하나를 선택합니다.

    **일반 문자열로 변환** 을 선택합니다.

    ![일반 문자열로 변환](media/convert-to-regular-string.png)

    **축자 문자열로 변환** 을 선택합니다.

    ![축자 문자열로 변환](media/convert-to-verbatim-string.png)

## <a name="see-also"></a>참조

- [리팩터링](../refactoring-in-visual-studio.md)