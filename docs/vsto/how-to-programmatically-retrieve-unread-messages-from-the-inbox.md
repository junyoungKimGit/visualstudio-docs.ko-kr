---
title: 프로그래밍 방식으로 받은 편지함에서 읽지 않은 메시지 가져오기
description: Visual Studio를 사용 하 여 Microsoft Outlook의 받은 편지함에서 읽지 않은 메시지를 프로그래밍 방식으로 검색 하는 방법을 알아봅니다.
ms.custom: SEO-VS-2020
ms.date: 02/02/2017
ms.topic: how-to
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- e-mail [Office development in Visual Studio], unread mail
- Outlook [Office development in Visual Studio], unread mail
- unread e-mail
- mail items [Office development in Visual Studio], unread mail
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: b6dae629c008c04f7ee9fb66b9dbc5f8f31e53d4
ms.sourcegitcommit: 4bd2b770e60965fc0843fc25318a7e1b46137875
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/15/2020
ms.locfileid: "97528260"
---
# <a name="how-to-programmatically-retrieve-unread-messages-from-the-inbox"></a>방법: 프로그래밍 방식으로 받은 편지함에서 읽지 않은 메시지 검색
  이 예제에서는 Outlook **받은 편지함** 에서 읽지 않은 전자 메일 메시지를 검색 하 고 항목 수를 표시 합니다.

 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]

## <a name="example"></a>예제
 [!code-vb[Trin_Outlook_RL_UnreadItems#1](../vsto/codesnippet/VisualBasic/Trin_Outlook_RL_UnreadItems/thisaddin.vb#1)]
 [!code-csharp[Trin_Outlook_RL_UnreadItems#1](../vsto/codesnippet/CSharp/Trin_Outlook_RL_UnreadItems/thisaddin.cs#1)]

## <a name="see-also"></a>참고 항목
- [메일 항목 작업](../vsto/working-with-mail-items.md)
- [VSTO 추가 기능 프로그래밍 시작](../vsto/getting-started-programming-vsto-add-ins.md)
- [방법: 프로그래밍 방식으로 전자 메일 항목 만들기](../vsto/how-to-programmatically-create-an-e-mail-item.md)
- [방법: 프로그래밍 방식으로 전자 메일 보내기](../vsto/how-to-programmatically-send-e-mail-programmatically.md)
- [방법: 프로그래밍 방식으로 전자 메일 메시지를 받을 때 작업 수행](../vsto/how-to-programmatically-perform-actions-when-an-e-mail-message-is-received.md)
