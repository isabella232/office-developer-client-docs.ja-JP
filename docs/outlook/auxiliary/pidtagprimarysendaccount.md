---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: メッセージのプライマリ accountsendstamp を指定します。
ms.openlocfilehash: b4d0188d75cdf03a78c198377c03a885fce3654b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601234"
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

