---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: メッセージの第 2 の accountsendstamp を指定します。
ms.openlocfilehash: 63d98382ff8a5a545cdb015c089c7b0a38926138
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799560"
---
# <a name="pidtagnextsendacct"></a>PidTagNextSendAcct

メッセージのサブ アカウントの「送信」スタンプを指定します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_NEXT_SEND_ACCT  <br/> |
|識別子:  <br/> |0x0E29  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |Outlook アプリケーション  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、MAPI のメッセージ オブジェクトに適用されます。 受信したメッセージは、サブ アカウントの「送信」タイムスタンプは、プライマリ アカウントを使用して転送、または返信を送信できない場合、転送または返信を送信するアカウントを示します。 、送信メッセージのスタンプを「送信」サブ アカウントをプライマリ アカウントでメッセージを送信できない場合にメッセージを送信するアカウントを決定します。 その値が、 [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) 、 [IOlkAccount](iolkaccount.md)のインターフェイス、メッセージが送信されているアカウントからです。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)
- [MAPI プロパティ](http://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [PidTagNextSendAcct 標準プロパティ](http://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

