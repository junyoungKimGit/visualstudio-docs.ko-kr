---
title: Command-Line 스위치 추가 | Microsoft Docs
description: devenv.exe 명령이 실행 될 때 VSPackage에 적용 되는 명령줄 스위치를 추가 하는 방법에 대해 알아봅니다.
ms.custom: SEO-VS-2020
ms.date: 11/04/2016
ms.topic: how-to
helpviewer_keywords:
- command-line switches, adding
- command-line switches, retrieving
- IVsAppCommandLine::GetOption method
- command line, switches
ms.assetid: 8bbbd87e-76fe-4fb5-8ef9-65f5e31967cf
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0eefb532380badcf917f6d512bc5b41ebb96b1d1
ms.sourcegitcommit: d6207a3a590c9ea84e3b25981d39933ad5f19ea3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/24/2020
ms.locfileid: "95597732"
---
# <a name="add-command-line-switches"></a>명령줄 스위치 추가
*devenv.exe* 실행 될 때 VSPackage에 적용 되는 명령줄 스위치를 추가할 수 있습니다. <xref:Microsoft.VisualStudio.Shell.ProvideAppCommandLineAttribute>스위치 이름과 해당 속성을 선언 하는 데 사용 합니다. 이 예제에서는 인수 없이 **Addcommandswitchpackage** 라는 VSPackage 라는 하위 클래스에 대해 MySwitch 스위치를 추가 하 고 VSPackage를 자동으로 로드 합니다.

```csharp
[ProvideAppCommandLine("MySwitch", typeof(AddCommandSwitchPackage), Arguments = "0", DemandLoad = 1)]
```

 명명 된 매개 변수는 다음 설명에 나와 있습니다.

|속성|Description|
|-|-|
| 인수 | 스위치에 대 한 인수 개수입니다. "*" 또는 인수 목록 일 수 있습니다. |
| DemandLoad | VSPackage가 1로 설정 되어 있으면 자동으로 로드 하 고 그렇지 않으면 0으로 설정 합니다. |
| HelpString | **Devenv/?** 를 사용 하 여 표시할 문자열의 도움말 문자열 또는 리소스 ID입니다. |
| 속성 | 스위치입니다. |
| PackageGuid | 패키지의 GUID입니다. |

 인수의 첫 번째 값은 일반적으로 0 또는 1입니다. 특수 값 ' * '를 사용 하 여 명령줄의 전체 나머지가 인수 임을 나타낼 수 있습니다. 이는 사용자가 디버거 명령 문자열을 전달 해야 하는 디버깅 시나리오에 유용할 수 있습니다.

 DemandLoad 값은 `true` (1) 또는 `false` (0) VSPackage가 자동으로 로드 되어야 함을 나타냅니다.

 HelpString 값은 **devenv/?** 에 표시 되는 문자열의 리소스 ID입니다. 도움말 표시. 이 값은 "#nnn" 형식 이어야 합니다. 여기서 nnn은 정수입니다. 리소스 파일의 문자열 값은 줄 바꿈 문자로 끝나야 합니다.

 이름 값은 스위치의 이름입니다.

 PackageGuid 값은이 스위치를 구현 하는 패키지의 GUID입니다. IDE는이 GUID를 사용 하 여 명령줄 스위치가 적용 되는 레지스트리의 VSPackage을 찾습니다.

## <a name="retrieve-command-line-switches"></a>명령줄 스위치 검색
 패키지가 로드 되 면 다음 단계를 완료 하 여 명령줄 스위치를 검색할 수 있습니다.

1. VSPackage의 구현에서 <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.SetSite%2A> `QueryService` 에 대해를 호출 <xref:Microsoft.VisualStudio.Shell.Interop.SVsAppCommandLine> 하 여 인터페이스를 가져옵니다 <xref:Microsoft.VisualStudio.Shell.Interop.IVsAppCommandLine> .

2. <xref:Microsoft.VisualStudio.Shell.Interop.IVsAppCommandLine.GetOption%2A>을 호출 하 여 사용자가 입력 한 명령줄 스위치를 검색 합니다.

   다음 코드에서는 MySwitch 명령줄 스위치가 사용자에 의해 입력 되었는지 확인 하는 방법을 보여 줍니다.

```csharp
IVsAppCommandLine cmdline = (IVsAppCommandLine)GetService(typeof(SVsAppCommandLine));

int isPresent = 0;
string optionValue = "";

cmdline.GetOption("MySwitch", out isPresent, out optionValue);
```

 패키지가 로드 될 때마다 명령줄 스위치를 확인 하는 것은 사용자의 책임입니다.

## <a name="see-also"></a>참고 항목
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsAppCommandLine>
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.SetSite%2A>
- [Devenv 명령줄 스위치](../ide/reference/devenv-command-line-switches.md)
- [CreatePkgDef 유틸리티](../extensibility/internals/createpkgdef-utility.md)
- [.Pkgdef 파일](https://devblogs.microsoft.com/visualstudio/whats-a-pkgdef-and-why/)
