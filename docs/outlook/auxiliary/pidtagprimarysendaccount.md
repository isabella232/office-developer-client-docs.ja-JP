---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: メッセージの主要な accountsendstamp を指定します。
ms.openlocfilehash: f94ac104a77e8400909dc06db44ce8ca03e4653f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799554"
---
# <a name="pidtagprimarysendaccount"></a>PidTagPrimarySendAccount

メッセージをプライマリ アカウントの「送信」スタンプを指定します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_PRIMARY_SEND_ACCOUNT  <br/> |
|識別子:  <br/> |0x0E28  <br/> |
|データを入力します。  <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |Account  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、MAPI のメッセージ オブジェクトに適用されます。 受信したメッセージは、プライマリ アカウントの「送信」スタンプはアカウントには、転送または返信を送信するかを示します。 送信メッセージでは、メッセージを送信するアカウントを決定します。 その値が、 [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) 、 [IOlkAccount](iolkaccount.md)のインターフェイス、メッセージが送信されているアカウントからです。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)
- [MAPI プロパティ](http://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [PidTagPrimarySendAccount の標準的なプロパティ](http://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

