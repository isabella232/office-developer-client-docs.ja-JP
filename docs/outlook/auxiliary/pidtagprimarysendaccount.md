---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: メッセージのプライマリ accountsendstamp を指定します。
ms.openlocfilehash: 902c71bd4a1bd5a25ab50c4b26bcfa6d5e8489e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327707"
---
# <a name="pidtagprimarysendaccount"></a>PidTagPrimarySendAccount

メッセージのプライマリ アカウント "send" スタンプを指定します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PRIMARY_SEND_ACCOUNT  <br/> |
|識別子:  <br/> |0x0E28  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |取引  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、MAPI メッセージ オブジェクトに適用されます。 受信したメッセージの場合、プライマリ アカウントの "送信" スタンプは、転送するアカウントまたは返信を送信するアカウントを示します。 送信メッセージの場合、メッセージを送信するアカウントを決定します。 その値は [、PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) が送信されるアカウントの [IOlkAccount](iolkaccount.md) インターフェイスからの値です。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)
- [MAPI のプロパティ](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [PidTagPrimarySendAccount 標準プロパティ](https://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

