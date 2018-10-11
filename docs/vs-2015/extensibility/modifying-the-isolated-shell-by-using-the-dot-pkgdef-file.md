---
title: 사용 하 여 격리 셸 수정 합니다. Pkgdef 파일 | Microsoft Docs
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
- Visual Studio shell, isolated mode%2C .pkgdef file
ms.assetid: 69e8f78e-bcf1-46cb-8866-7de37d134997
caps.latest.revision: 28
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f70036f91eb52d85054465e6eea9f82672d851f6
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "47553412"
---
# <a name="modifying-the-isolated-shell-by-using-the-pkgdef-file"></a>사용 하 여 격리 셸 수정 합니다. Pkgdef 파일
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

이 항목의 최신 버전에서 찾을 수 있습니다 [의 격리 셸을 사용 하 여 수정 합니다. Pkgdef 파일](https://docs.microsoft.com/visualstudio/extensibility/modifying-the-isolated-shell-by-using-the-dot-pkgdef-file)합니다.  
  
.Pkgdef 파일에는 격리 셸 응용 프로그램을 사용자 지정 하는 데 사용할 수 있는 설정을 지원 합니다. 응용 프로그램이 컴퓨터에 설치 되 고 응용 프로그램을 시작 하는 경우 Visual Studio shell에서 참조 되는 경우 생성 되는 값을 지정 합니다. 설정은 해당 레지스트리 키를 기준으로 파일에 구성 됩니다.  
  
> [!WARNING]
>  Visual Studio를 시작 하는 경우 VSPackage의.vsixmanifest 파일에서 선언 되지 않은.pkgdef 파일이 검색 되지 않습니다 note 합니다.  
  
 .Pkgdef 파일에는 식별 되는 각 키로 하거나 섹션이 포함 되어 있습니다. `[$RootKey$]` 나 `[$RootKey$\` *하위 키*`]`을 $RootKey$ 응용 프로그램에 대 한 루트 키입니다.  
  
 각 섹션에는 다음 형식으로 된 이름/값 쌍: `"` *ValueName*`"=`*값*합니다.  
  
 값은 따옴표로 묶인 문자열 또는 dword로 표현 되는 32 비트 정수입니다. 값에는 다음 제약 조건이:  
  
-   모든 dword 값은 16 진수 형식, 예를 들어 `dword:00000001`합니다.  
  
     부울 값을 1 true 나타내고 0은 false입니다.  
  
-   예를 들어 레지스트리 형식으로 모든 GUID 문자열은 `"{00000000-0000-0000-0000-000000000000}"`합니다.  
  
-   모든 지역화 가능 리소스 식별자가 형식 "@*resourceID*" 또는 "#*resourceID*" 여기서 *resourceID* 응용 프로그램 UI 패키지에 있는 리소스 식별자 예를 들어 `"@102"`합니다. 응용 프로그램 UI 패키지는 AppLocalizationPackage 설정에서 참조 되는 패키지가입니다.  
  
 예를 들어 개체에 적용된  
  
```  
"HideSolutionConcept"=dword:00000001  
"DefaultDebugEngine"="{00000000-0000-0000-0000-000000000000}"  
```  
  
 .Pkgdef 파일에 주석을 추가할 수 있습니다. 한 줄 주석을 처음 두 문자와 슬래시 두 개를 가집니다.  
  
 대체 문자열의 목록을 참조 하세요. [대체 문자열에 사용 됩니다. Pkgdef 및 합니다. Pkgundef 파일](../extensibility/substitution-strings-used-in-dot-pkgdef-and-dot-pkgundef-files.md)합니다.  
  
 다음 섹션에서는 Visual Studio shell 격리 모드에서의 동작에 영향을 주는 특정 레지스트리 값을 설명 합니다. 또한이 파일에 응용 프로그램에 대 한 추가 레지스트리 값을 정의할 수 있습니다.  
  
> [!NOTE]
>  .Pkgdef 파일에서 설정을 제공 하지 않으면 해당 항목이 레지스트리에 이루어집니다.  
  
## <a name="settings"></a>설정  
 다음 표에서 [$RootKey$] 아래에 정의 된 값을 보여 줍니다.  
  
|이름|형식|값|  
|----------|----------|-----------|  
|AddinsAllowed|dword|추가 기능을 로드할 수 있으면 true입니다. 그렇지 않으면 false입니다.<br /><br /> 기본값은 true입니다.|  
|AllowsDroppedFilesOnMainWindow|dword|주 창에서 끌어 놓은 파일;를 사용할 수 있으면 true입니다. 그렇지 않으면 false입니다. 주 창에서 삭제 된 파일을 사용 하 여 열은 <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShellOpenDocument.OpenDocumentViaProject%2A> 메서드. 사용 하 여 문서를 열기와 동일 합니다 **열려** 명령을 **파일** 응용 프로그램에서 메뉴.<br /><br /> 기본값은 true입니다.|  
|AppIcon|string|프로그램 아이콘의 전체 경로입니다. 응용 프로그램 이름의 왼쪽에 제목 표시줄에이 아이콘이 표시 됩니다.<br /><br /> 기본값은 "$ $RootFolder\\*solutionName*.ico" 여기서 *solutionName* 응용 프로그램 솔루션 파일의 이름입니다.|  
|AppLocalizationPackage|string|응용 프로그램에 대 한 UI 위성 어셈블리를 포함 하는 VSPackage의 GUID입니다. 이 VSPackage.vsct 파일의 컴파일된 버전을 포함 하 고 다른 지역화 된 문자열을 포함할 수 있습니다. 기능 집합 및 메뉴 명령 그룹을 사용 하도록 설정 또는 UI 프로젝트.vsct 파일의 설정을 변경 하 여 사용 하지 않도록 설정 수 있습니다.<br /><br /> 기본값은 "{*vsUiPackageGuid*}", 여기서 *vsUiPackageGuid* UI 응용 프로그램 패키지에 할당 된 GUID입니다.|  
|응용 프로그램 이름|string|응용 프로그램의 이름입니다. 이름이 응용 프로그램 창의 제목 표시줄에 나타납니다.<br /><br /> 기본값은 응용 프로그램 솔루션 파일의 이름입니다.|  
|CommandLineLogo|string|콘솔 창에는 응용 프로그램을 실행할 때 배너 텍스트입니다. 이 설정은 명령줄 빌드 작업을 지 원하는 응용 프로그램 에서만 적용 됩니다.<br /><br /> 기본값은 "*companyName * * solutionName* 버전 1.0입니다.", 여기서 *companyName* 은 Windows를 설치할 때 제공 하는 회사의 이름 및 *solutionName*응용 프로그램 솔루션 파일의 이름입니다.|  
|DefaultDebugEngine|string|응용 프로그램을 사용 하도록 엔진을 디버그 하는 기본값의 GUID입니다.<br /><br /> 참고: 응용 프로그램에서 기본 디버그 엔진을 지정 하지 않았는지 빈 GUID (모두 0)를 나타냅니다. 그러면 디버거를 사용 하려면 디버그 엔진을 선택 합니다.<br /><br /> 기본값은 "{00000000-0000-0000-0000-000000000000}"입니다.|  
|DefaultHomePage|string|내부 웹 브라우저 창에 대 한 기본 홈 페이지 URL입니다.<br /><br /> 경우는 **홈페이지** 옵션은 응용 프로그램에서 사용 가능한 다음이 설정을 옵션의 기본 상태에도 영향을 줍니다. 자세한 내용은 [웹 브라우저, 환경, 옵션 대화 상자](../ide/reference/web-browser-environment-options-dialog-box.md)합니다.<br /><br /> 기본값은 Windows를 설치할 때 제공 하는 회사의 URL입니다.|  
|DefaultProjectsLocation|string|기본 프로젝트 폴더의 전체 경로입니다. 예를 들어 개체에 적용된<br /><br /> `"DefaultProjectsLocation"="$MyDocuments$\MyVSShellStub\Projects"`<br /><br /> 경우는 **Visual Studio 프로젝트 위치** 옵션은 응용 프로그램에서 사용 가능한 다음이 설정을 옵션의 기본 상태에도 영향을 줍니다. 자세한 내용은 [NIB: 일반, 프로젝트 및 솔루션, 옵션 대화 상자](http://msdn.microsoft.com/en-us/8f8e37e8-b28d-4b13-bfeb-ea4d3312aeca)합니다.<br /><br /> 기본값은 "$MyDocuments$\\*solutionName*", 여기서 *solutionName* 응용 프로그램 솔루션 파일의 이름입니다.|  
|DefaultSearchPage|string|내부 웹 브라우저 창에 대 한 기본 검색 페이지 URL입니다.<br /><br /> 경우는 **검색 페이지** 옵션은 응용 프로그램에서 사용 가능한 다음이 설정을 옵션의 기본 상태에도 영향을 줍니다. 자세한 내용은 [웹 브라우저, 환경, 옵션 대화 상자](../ide/reference/web-browser-environment-options-dialog-box.md)합니다.<br /><br /> 기본값은 "http://search.live.com"입니다.|  
|DefaultUserFilesFolderRoot|string|현재 사용자를 기준으로 사용자 폴더의 이름을 내 문서 폴더입니다.<br /><br /> 기본값은 응용 프로그램 솔루션 파일의 이름입니다.|  
|DisableOutputWindow|dword|사용 안 함으로 격리 셸 출력 창에 처리 해야 하는지 여부를 나타냅니다.<br /><br /> 이 값 설정 하는 경우 true이 고, Visual Studio 솔루션 빌드 관리자 출력에 표시 되지 않습니다 합니다 **출력** 창과 숨깁니다 합니다 **빌드를 시작할 때 출력 창 표시** 확인란을  **프로젝트 및 솔루션** 범주에는 **옵션** 대화 상자.<br /><br /> 기본값은 false입니다.|  
|HideMiscellaneousFilesByDefault|dword|숨기기 하려면 true로 설정 합니다 **기타 파일** 에서 기본적으로 폴더 **솔루션 탐색기**, 그렇지 않으면 false입니다.<br /><br /> 경우는 **솔루션 탐색기에 기타 파일 표시** 옵션은 응용 프로그램에서 사용 가능한 다음이 설정을 옵션의 기본 상태에도 영향을 줍니다. 자세한 내용은 [문서, 환경, 옵션 대화 상자](../ide/reference/documents-environment-options-dialog-box.md)합니다.<br /><br /> 기본값은 false입니다.|  
|HideSolutionConcept|dword|모든 프로젝트 독립적으로 프로젝트를 만들고 솔루션 및 프로젝트의 독립 실행형 솔루션 관련 명령을 기본적으로 숨깁니다 true 그렇지 않으면 false입니다.<br /><br /> 경우는 **솔루션 항상 표시** 옵션은 응용 프로그램에서 사용 가능한 다음이 설정을 옵션의 기본 상태에도 영향을 줍니다. 자세한 내용은 [NIB: 일반, 프로젝트 및 솔루션, 옵션 대화 상자](http://msdn.microsoft.com/en-us/8f8e37e8-b28d-4b13-bfeb-ea4d3312aeca)합니다.<br /><br /> 기본값은 false입니다.|  
|NewProjDlgInstalledTemplatesHdr|string|Visual Studio nstalled 템플릿 헤더에 대 한 이름을 합니다 **템플릿을** 목록에 **새 프로젝트** 대화 상자. 이것이 응용 프로그램 UI 패키지에서 로드 되는 지역화할 수 있는 리소스 식별자 또는 문자열입니다.<br /><br /> 기본값은 "*solutionName* 설치 되어 있는 템플릿", 여기서 *solutionName* 응용 프로그램 솔루션 파일의 이름입니다.|  
|NewProjDlgSlnTreeNodeTitle|string|에 대 한 이름을 **Visual Studio 솔루션** 에서 노드를 **프로젝트 형식** 에서 트리를 **새 프로젝트** 대화 상자. 이것이 응용 프로그램 UI 패키지에서 로드 되는 지역화할 수 있는 리소스 식별자 또는 문자열입니다.<br /><br /> 기본값은 "*solutionName* 설치 되어 있는 템플릿", 여기서 *solutionName* 응용 프로그램 솔루션 파일의 이름입니다.|  
|SolutionFileCreatorIdentifier|string|응용 프로그램에서 생성 되는 솔루션 파일의 두 번째 줄으로 표시 되는 응용 프로그램 식별자입니다. 이 줄은 파일을 만든 응용 프로그램을 나타냅니다. 규칙에 따라이 값에는 응용 프로그램 및 응용 프로그램의 버전 번호의 이름을 둘 다 포함 됩니다. 예를 들어 개체에 적용된<br /><br /> `"SolutionFileCreatorIdentifier"="MyVSShellStub Solution File, Format Version 10.00"`<br /><br /> Visual Studio 솔루션 파일을 열에 대 한 기본 프로그램 인 VSLauncher.exe 프로그램을 솔루션 파일을 여는 Visual Studio의 버전을 확인 하려면이 두 번째 줄을 사용 합니다. 응용 프로그램에는 자체 시작 관리자는 연결 된 솔루션 파일을 처리 해야 합니다. 시작 관리자 사용할 수도이 두 번째 줄 솔루션 파일에는 버전의 솔루션을 열려면 응용 프로그램 확인 하려면.<br /><br /> 참고: Visual Studio VSLauncher.exe 프로그램 격리 셸 응용 프로그램에서 생성 된.sln 파일을 처리 하지 않습니다.<br /><br /> 기본값은 "*solutionName* 솔루션 파일 형식 버전 $10.00" 여기서 *solutionName* 응용 프로그램 솔루션 파일의 이름입니다.|  
|SolutionFileExt|string|응용 프로그램에 대 한 솔루션 파일 이름 확장명입니다. 고유한 파일 이름 확장명 (not.sln)을 선택 하는 것이 좋습니다.<br /><br /> 기본값은 "*solutionName*_sln" 여기서 *solutionName* 응용 프로그램 솔루션 파일의 이름입니다.|  
|SplashScreenBitmap|string|응용 프로그램에 대 한 시작 화면에 대 한 비트맵 파일의 전체 경로입니다.<br /><br /> 기본값은 "$RootFolder$\Splash.bmp"입니다.|  
|ThisVersionDTECLSID|string|응용 프로그램에 대 한 자동화 개체의 클래스 식별자 (CLSID)입니다.<br /><br /> 응용 프로그램 자동화 개체는 구현 하 고 Visual Studio shell 자동화 모델에서 응용 프로그램에 대 한 최상위 개체는 <xref:EnvDTE._DTE?displayProperty=fullName> 인터페이스입니다.<br /><br /> 응용 프로그램 자동화 개체 HKEY_CLASSES_ROOT\CLSID 레지스트리 키 아래에 올바르게 등록 되어 있으면 사용할 수는 [CComPtrBase::CoCreateInstance](http://msdn.microsoft.com/library/c0965041-6cb6-40c5-b272-2b99f02668a6) 함수를 직접 응용 프로그램의 인스턴스를 만듭니다.<br /><br /> Visual Studio 셸은이 CLSID를 사용 하 여 ACTIVEOBJECT_WEAK 플래그를 사용 하 여 응용 프로그램 자동화 개체의 개체 테이블 ROT (실행)를 등록 합니다. 이렇게 하면 사용할 수 있습니다 합니다 [GetActiveObject](http://msdn.microsoft.com/en-us/a276e30c-6a7f-4cde-9639-21a9f5170b62)응용 프로그램의 실행 인스턴스에 대 한 포인터를 검색 하는 함수입니다. 또한 응용 프로그램 자동화 개체에 대 한 ProgID를 정의 하는 경우 다음 Visual Studio shell도 등록 응용 프로그램의 각 인스턴스에 ROT에서 폼의 항목 모니커를 사용 하 여 *progID*:*processID* , 여기서 *progID* 는 응용 프로그램 자동화 개체의 ProgID 및 *processID* 응용 프로그램의 해당 인스턴스에 대 한 프로세스 식별자입니다. 예를 들어 다음과 같이 모니커를 만듭니다.<br /><br /> `CreateItemMoniker(L"!",`  *instanceString* `, &instanceMoniker)`<br /><br /> 여기서 `instanceString` 되는 *progID*:*processID* 문자열입니다. 사용할 수 있습니다 다음 `instanceMoniker` ROT GetObject 함수 인스턴스를 사용 하 여 합니다.<br /><br /> ThisVersionDTECLSID 설정이 생략 되 면 다음 응용 프로그램 구성 요소 개체 모델 (COM)를 통해를 노출 되지 않습니다. 이 경우 호출 하 여 응용 프로그램의 인스턴스를 만들 수 없습니다는 [CComPtrBase::CoCreateInstance](http://msdn.microsoft.com/library/c0965041-6cb6-40c5-b272-2b99f02668a6) 함수 및 ROT에 등록할 수 없습니다.<br /><br /> VSPackage의 각 버전에는 다른 CLSID 있어야 합니다.<br /><br /> 기본값은 응용 프로그램의 자동화 개체에 대 한 Visual Studio에서 생성 하는 GUID입니다.|  
|ThisVersionSolutionCLSID|string|응용 프로그램에 대 한 솔루션 개체의 CLSID입니다.<br /><br /> 구현 하 고 응용 프로그램 인스턴스의 현재 열려 있는 솔루션에 대 한 정보를 포함 하는 솔루션 자동화 개체는 <xref:EnvDTE._Solution?displayProperty=fullName> 인터페이스입니다.<br /><br /> 솔루션 자동화 개체 HKEY_CLASSES_ROOT\CLSID 레지스트리 키 아래에 올바르게 등록 되어 있으면 사용할 수는 [CComPtrBase::CoCreateInstance](http://msdn.microsoft.com/library/c0965041-6cb6-40c5-b272-2b99f02668a6) 직접 응용 프로그램에 대 한 솔루션 개체를 만드는 함수입니다.<br /><br /> Visual Studio 셸은이 CLSID를 사용 하 여 ACTIVEOBJECT_WEAK 플래그를 사용 하 여 ROT에 솔루션 자동화 개체를 등록 합니다.<br /><br /> 이 설정을 생략 되 면 솔루션 클래스를 사용 하 여 구성 요소 개체 모델 (COM) 등록 되지 않은 하 고 호출 하 여 솔루션 개체를 만들 수 없습니다 경우 합니다 [CComPtrBase::CoCreateInstance](http://msdn.microsoft.com/library/c0965041-6cb6-40c5-b272-2b99f02668a6) 함수 및에 등록할 수 없습니다 ROT 합니다.<br /><br /> 기본값은 응용 프로그램의 솔루션 개체에 대 한 Visual Studio에서 생성 하는 GUID입니다.|  
|UserFilesSubFolderName|string|사용자의 내 문서 폴더는 응용 프로그램 사용자 파일 및 하위 폴더를 만듭니다 하위 폴더의 이름입니다.<br /><br /> 기본값은 응용 프로그램 솔루션 파일의 이름입니다.|  
|UserOptsFileExt|string|응용 프로그램에 대 한 솔루션 사용자 옵션 파일에 대 한 확장입니다.<br /><br /> 기본값은 응용 프로그램 솔루션 파일의 이름입니다.|  
  
## <a name="binding-path-settings"></a>바인딩 경로 설정  
 [$RootKey$ \BindingPaths\\{00000000-0000-0000-0000-000000000000}] 키 셸에서 어셈블리에 대 한 확인 하는 디렉터리의 목록을 포함 합니다. 이러한 디렉터리는 셸 응용 프로그램에 대 한 전용 어셈블리를 검색 하는 디렉터리 목록에 추가 됩니다.  
  
 기본적으로 바인딩 경로 항목이 없는.pkgdef 파일에 추가 됩니다. 그러나 Visual Studio 설치 디렉터리의 다음 하위 디렉터리는 레지스트리에서 응용 프로그램 바인딩 경로 목록에 자동으로 추가 됩니다.  
  
-   Common7\IDE\  
  
-   Common7\IDE\\\PrivateAssemblies  
  
-   Common7\IDE\\\PublicAssemblies  
  
 디렉터리에 바인딩 경로를 추가 하려면 폼의 항목을 추가 "*directoryName*"="", 여기서 *directoryName* 절대 경로입니다. 예를 들어 개체에 적용된  
  
```  
[$RootKey$\BindingPaths\{00000000-0000-0000-0000-000000000000}]  
"$RootFolder$\directory1"=""  
"%CommonProgramFiles%\directory2"=""  
```  
  
## <a name="profile-settings"></a>프로필 설정  
 다음 표에서 [$RootKey$ \Profile]에서 연결 된 각 패키지에 대해 정의 된 값을 보여 줍니다.  
  
|이름|형식|값|  
|----------|----------|-----------|  
|AutoSaveFile|string|응용 프로그램 자동 저장 된 파일을 저장 하는 디렉터리입니다.<br /><br /> 기본값은 "$RootFolder$\Profiles\CurrentSettings.vssettings"입니다.|  
  
## <a name="package-satellite-dll-settings"></a>패키지 위성 DLL 설정  
 다음 표에 정의 된 값 [$RootKey$ \Packages\\{0}*vsPackageGuid*} \SatelliteDll] 위성 DLL 연결 된 각 패키지의 위치 *vsPackageGuid* 연결 된 패키지의 GUID입니다.  
  
|이름|형식|값|  
|----------|----------|-----------|  
|DllName|string|DLL의 파일 이름입니다.<br /><br /> 기본값은 "*solutionName*ui.dll" 여기서 *solutionName* 응용 프로그램 솔루션 파일의 이름입니다.|  
|Path|string|위성 DLL을 포함 하는 디렉터리입니다.<br /><br /> 기본값은 "$PackageFolder$"입니다.|  
  
## <a name="package-menu-item-settings"></a>패키지 메뉴 항목 설정  
 [$RootKey$ \Menus] 레지스트리 키를 응용 프로그램에 대 한 UI 리소스 파일을 정의합니다.  
  
 메뉴 항목 값 형식 이어야 "{*vsUiPackageGuid*}"=" *resourceId*하십시오 *versionNumber*" 여기서 *vsUiPackageGuid* 의 GUID입니다 응용 프로그램 UI 패키지 *resourceId* 은 UI 요소를 포함 하는 CTMENU 리소스의 리소스 식별자 및 *versionNumber* 는 CTMENU 가상 버전 번호입니다 리소스입니다. 자세한 내용은 [Interop 어셈블리 명령 처리기 등록](../extensibility/internals/registering-interop-assembly-command-handlers.md)합니다.  
  
 기본적으로 메뉴 항목의 항목을 응용 프로그램 UI 패키지의.pkgdef 파일에 만들어집니다.  
  
 메뉴 항목을 제공 하 고 응용 프로그램의 일부로 배포 되는 각 패키지에 대 한 패키지에 대 한 메뉴 항목을 추가 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [격리 셸 사용자 지정](../extensibility/customizing-the-isolated-shell.md)   
 [.pkgundef 파일](../extensibility/modifying-the-isolated-shell-by-using-the-dot-pkgundef-file.md)
