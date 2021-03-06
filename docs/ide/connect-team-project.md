---
title: 팀 탐색기의 프로젝트에 연결
description: Visual Studio에서 팀 탐색기를 사용하여 팀 구성원과 함께 프로젝트를 개발하고 관리하는 방법을 알아봅니다.
ms.custom: SEO-VS-2020
ms.date: 11/17/2020
ms.topic: conceptual
ms.author: tglee
author: TerryGLee
ms.manager: jillfra
ms.openlocfilehash: fd482bd2225025b5cd8a14f0387e938626fad6d5
ms.sourcegitcommit: 66cda27b63c9b55782b1db223a6dbda9f8cabe13
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/21/2020
ms.locfileid: "95006317"
---
# <a name="connect-to-projects-in-team-explorer"></a>팀 탐색기의 프로젝트에 연결

::: moniker range="vs-2017"

**팀 탐색기** 도구 창을 사용하여 프로젝트를 개발하고 사용자, 팀 또는 프로젝트에 할당된 작업을 관리하기 위해 다른 팀 구성원과 코드 작업을 조정합니다. **팀 탐색기** 는 Visual Studio를 Git 및 GitHub 리포지토리, TFVC(Team Foundation 버전 제어) 리포지토리 및 [Azure DevOps Services](/azure/devops/user-guide/what-is-azure-devops-services) 또는 온-프레미스 [Azure DevOps 서버](/azure/devops/index-all)(이전의 TFS로 알려짐)에 호스팅된 프로젝트와 연결합니다. 소스 코드, 작업 항목 및 빌드를 관리할 수 있습니다.

::: moniker-end

::: moniker range="vs-2019"

**팀 탐색기** 도구 창을 사용하여 프로젝트 개발 및 사용자, 팀 또는 프로젝트에 할당된 작업 관리를 위해 다른 팀 구성원과 코드 작업을 조정할 수 있습니다.

> [!IMPORTANT]
> Visual Studio 2019 [버전 16.8](/visualstudio/releases/2019/release-notes/) 최근 릴리스에서는 이제 새로운 Git 버전 제어 환경이 기본적으로 설정되어 있습니다. 하지만 팀 탐색기를 계속 사용하려면 **도구** > **옵션** > **환경** > **미리 보기 기능** 으로 이동한 다음 **새 Git 사용자 환경** 확인란을 토글합니다. 자세한 내용은 [Visual Studio의 Git 환경](git-with-visual-studio.md) 페이지를 참조하세요.

**팀 탐색기** 는 Visual Studio를 Git 및 GitHub 리포지토리, TFVC(Team Foundation 버전 제어) 리포지토리 및 [Azure DevOps Services](/azure/devops/user-guide/what-is-azure-devops-services) 또는 온-프레미스 [Azure DevOps 서버](/azure/devops/index-all)(이전의 TFS로 알려짐)에 호스팅된 프로젝트와 연결합니다. 소스 코드, 작업 항목 및 빌드를 관리할 수 있습니다.

::: moniker-end

![Visual Studio의 팀 탐색기 홈 페이지](media/team-explorer/team-explorer.png "팀 탐색기 - Visual Studio의 홈 페이지.")

::: moniker range="vs-2017"

> [!TIP]
> Visual Studio를 열었지만 **팀 탐색기** 가 나타나지 않으면 메뉴 모음에서 **보기** > **팀 탐색기** 를 선택하거나 **Ctrl**+ **&#92;** , **Ctrl**+**M** 을 눌러 엽니다.

::: moniker-end

## <a name="connect-to-a-project-or-repository"></a>프로젝트 또는 리포지토리에 연결

**연결** 페이지에서 프로젝트 또는 리포지토리에 연결합니다.

![팀 탐색기에서 페이지 연결](media/team-explorer/connect.png "팀 탐색기 - Visual Studio의 연결 페이지.")

프로젝트에 연결하려면:

1. **연결 관리** 아이콘을 선택하여 **연결** 페이지를 엽니다.

   ![팀 탐색기에서 연결 단추 관리](media/team-explorer/manage-connections.png "팀 탐색기 - Visual Studio의 연결 관리 단추.")

1. **연결** 페이지에서 **연결 관리** > **프로젝트에 연결** 을 선택합니다.

   ![팀 탐색기의 프로젝트에 연결](media/team-explorer/connect-project.png "팀 탐색기 - Visual Studio의 프로젝트에 연결 옵션.")

> [!TIP]
> 리포지토리에서 프로젝트를 열려면 [리포지토리에서 프로젝트 열기](../get-started/tutorial-open-project-from-repo.md)를 참조하세요. 새 프로젝트를 만들거나 프로젝트에 사용자를 추가하려면 [프로젝트 만들기(Azure DevOps)](/azure/devops/organizations/projects/create-project) 및 [프로젝트 또는 팀에 사용자 추가(Azure DevOps)](/azure/devops/organizations/security/add-users-team-project)를 참조하세요.

## <a name="see-also"></a>참조

- [Visual Studio의 새로운 Git 환경](git-with-visual-studio.md)
- [자습서: 리포지토리에서 프로젝트 열기](../get-started/tutorial-open-project-from-repo.md)
- [팀 탐색기 참조](reference/team-explorer-reference.md)
- [프로젝트(Azure DevOps)에 연결](/azure/devops/organizations/projects/connect-to-projects)
- [Troubleshoot connecting to a project](/azure/devops/user-guide/troubleshoot-connection?view=azure-devops&preserve-view=true)(프로젝트 연결 문제 해결)
