---
title: PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 52003a4e-1b61-2965-5204-6601652dd15b
description: メッセージを配信したアカウントのアカウント スタンプを返します。
ms.openlocfilehash: aa81ce920cc448557bc23a0ba0fde603934f8e39
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572229"
---
# <a name="pidlidinternetaccountstamp"></a>PidLidInternetAccountStamp

メッセージを配信したアカウントのアカウント スタンプを返します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidInetAcctStamp  <br/> |
|プロパティ セット:  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x00008581  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには、メッセージを配信したアカウントの Account Management API プロパティ [PROP_ACCT_STAMP同じ](prop_acct_stamp.md) 値を含む必要があります。 
  
メッセージ ストア プロバイダーは、この名前付きプロパティと [PidLidInternetAccountName](pidlidinternetaccountname.md) を公開して、次のアクションを実行します。 
  
- ユーザーが電子メールメッセージで [全員に返信] をクリックすると、Outlook はアカウントに関連付けられている電子メール アドレスを削除し、返信の受信者リストからメッセージにスタンプされます。 この動作は、この電子メール アドレスが元のメッセージの送信者である場合を使用しない限り発生します。 
    
- 既定では、Outlookメッセージにスタンプされたアカウントを通じて返信メッセージと転送メッセージが送信されます。
    
通常、Outlook プロトコル マネージャーはメッセージを配信し、Outlook は **PidLidInternetAccountName** プロパティと **PidLidInternetAccountStamp** プロパティを設定して、メッセージを配信したアカウントを示します。 ただし、メッセージ ストアがトランスポートと緊密に結合されている場合、Outlook プロトコル マネージャーはメッセージを配信し、Outlookプロパティを設定できません。 このシナリオでは、Outlook [IMAPIProp::GetIDsFromNames 関数を呼び出](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx)します。 メッセージ ストア プロバイダーがこれらの名前付きプロパティを公開する場合は **、IMAPIProp::GetIDsFromNames** を実装し、出力パラメーター  *lppPropTags*  を使用してプロパティ タグを返す必要があります。 Outlookこれらのプロパティ タグを使用して[IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx)メソッドを呼び出し、メッセージ ストア プロバイダーは目的のアカウントのアカウント名とスタンプを返します。 
  
これらの名前付きプロパティをサポートするために、ストア プロバイダーは、Outlook プロパティのプロパティ タグを取得するために **IMAPIProp::GetIDsFromNames** を使用する必要があります。 Outlookは **、IMAPIProp::GetIDsFromNames** の入力パラメーター *lppPropNames* によって示される配列の一部として渡される、この名前付きプロパティに対応する [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx)構造体の次の値を指定します。 
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_ID  <br/> |
|Kind.lID:  <br/> |dispidInetAcctStamp  <br/> |
   
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)
- [PidLidInternetAccountStamp 標準プロパティ](https://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)

