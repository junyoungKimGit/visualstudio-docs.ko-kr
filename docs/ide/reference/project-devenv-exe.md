---
title: -Project(devenv.exe)
description: Project devenv 명령줄 스위치를 사용하여 프로젝트를 빌드, 정리, 다시 빌드 또는 배포하기 위해 지정된 솔루션 구성 내에서 단일 프로젝트를 파악하는 방법을 알아봅니다.
ms.custom: SEO-VS-2020
ms.date: 12/10/2018
ms.topic: reference
helpviewer_keywords:
- /Project Devenv switch
- projects [Visual Studio], rebuilding
- projects [Visual Studio], building
- deployment projects, specifying
- Project Devenv switch (/Project)
- Devenv, /Project switch
- projects [Visual Studio], cleaning
ms.assetid: 8b07859c-3439-436d-9b9a-a8ee744eee30
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 90c1cdf37ddda7209b4f951e42ad07720e5cc40b
ms.sourcegitcommit: 967c2f8c1b3f805cf42c0246389517689d971b53
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/25/2020
ms.locfileid: "96040111"
---
# <a name="project-devenvexe"></a>/Project (devenv.exe)

빌드, 정리, 다시 빌드 또는 배포하도록 솔루션 구성 내에서 단일 프로젝트를 식별합니다.

## <a name="syntax"></a>구문

```shell
devenv SolutionName {/Build|/Clean|/Deploy|/Rebuild} [SolnConfigName [/Project ProjName [/ProjectConfig ProjConfigName]] [/Out OutputFilename]]
```

## <a name="arguments"></a>인수

- *SolutionName*

  필수 요소. 솔루션 파일의 전체 경로 및 이름입니다.

- {`/Build`|`/Clean`|`/Deploy`|`/Rebuild`}

  필수 요소. 프로젝트를 [빌드](build-devenv-exe.md), [정리](clean-devenv-exe.md), [배포](deploy-devenv-exe.md) 또는 [다시 빌드](rebuild-devenv-exe.md)합니다.

- *SolnConfigName*

  선택 사항입니다. *SolutionName* 에서 명명된 솔루션에 적용되는 솔루션 구성의 이름입니다(예: `Debug` 또는 `Release`). 둘 이상의 솔루션 플랫폼을 사용할 수 있는 경우 플랫폼(예: `Debug|Win32`)도 지정해야 합니다. 이 인수가 지정되지 않거나 빈 문자열(`""`)인 경우에는 솔루션의 활성 구성이 사용됩니다.

- `/Project` *ProjName*

  선택 사항입니다. 솔루션 내에 있는 프로젝트 파일의 경로와 이름입니다. 프로젝트의 표시 이름 또는 *SolutionName* 폴더에서 프로젝트 파일까지 상대 경로를 입력할 수 있습니다. 프로젝트 파일의 전체 경로와 이름을 입력할 수도 있습니다.

- `/ProjectConfig` *ProjConfigName*

  선택 사항입니다. 명명된 `/Project`에 적용할 프로젝트의 빌드 구성 이름입니다(예: `Debug` 또는 `Release`). 둘 이상의 솔루션 플랫폼을 사용할 수 있는 경우 플랫폼(예: `Debug|Win32`)도 지정해야 합니다.

- `/Out` *OutputFilename*

  선택 사항입니다. 도구의 출력을 보낼 파일의 이름입니다. 파일이 이미 있는 경우 출력은 파일의 끝에 추가됩니다.

## <a name="remarks"></a>설명

- `devenv` `/Build`, `/Clean`, `/Rebuild` 또는 `/Deploy` 명령의 일부로 사용해야 합니다.

- 공백을 포함하는 문자열은 큰따옴표로 묶습니다.

- 오류를 포함한 빌드에 대한 요약 정보는 **명령** 창 또는 `/Out` 스위치로 지정된 로그 파일에 표시할 수 있습니다.

## <a name="example"></a>예제

이 예제에서는 `MySolution` 내에 있는 `Debug` 프로젝트 빌드 구성을 사용하여 `CSharpWinApp` 프로젝트를 빌드합니다.

```shell
devenv "%USERPROFILE%\source\repos\MySolution\MySolution.sln" /build Debug /project "CSharpWinApp\CSharpWinApp.csproj" /projectconfig Debug
```

## <a name="see-also"></a>참고 항목

- [Devenv 명령줄 스위치](../../ide/reference/devenv-command-line-switches.md)
- [/ProjectConfig (devenv.exe)](../../ide/reference/projectconfig-devenv-exe.md)
- [/Build (devenv.exe)](../../ide/reference/build-devenv-exe.md)
- [/Clean (devenv.exe)](../../ide/reference/clean-devenv-exe.md)
- [/Rebuild (devenv.exe)](../../ide/reference/rebuild-devenv-exe.md)
- [/Deploy (devenv.exe)](../../ide/reference/deploy-devenv-exe.md)
- [/Out (devenv.exe)](../../ide/reference/out-devenv-exe.md)
