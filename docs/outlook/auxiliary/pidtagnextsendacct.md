---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: メッセージの第 2 の accountsendstamp を指定します。
ms.openlocfilehash: 3aa88a1fd5a73cc4ae2e990e6dad0697083bb694
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396478"
---
# <a name="pidtagnextsendacct"></a>PidTagNextSendAcct

メッセージのサブ アカウントの「送信」スタンプを指定します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_NEXT_SEND_ACCT  <br/> |
|識別子:  <br/> |0x0E29  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |Outlook アプリケーション  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、MAPI のメッセージ オブジェクトに適用されます。 受信したメッセージは、サブ アカウントの「送信」タイムスタンプは、プライマリ アカウントを使用して転送、または返信を送信できない場合、転送または返信を送信するアカウントを示します。 、送信メッセージのスタンプを「送信」サブ アカウントをプライマリ アカウントでメッセージを送信できない場合にメッセージを送信するアカウントを決定します。 その値が、 [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) 、 [IOlkAccount](iolkaccount.md)のインターフェイス、メッセージが送信されているアカウントからです。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)
- [MAPI プロパティ](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [PidTagNextSendAcct 標準プロパティ](https://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

