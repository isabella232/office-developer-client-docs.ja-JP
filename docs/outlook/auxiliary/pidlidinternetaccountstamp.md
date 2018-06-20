---
title: PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 52003a4e-1b61-2965-5204-6601652dd15b
description: メッセージを配信するアカウントのアカウントのタイムスタンプを返します。
ms.openlocfilehash: ba54bffb60a05a3b4a1ff30519960740af93ebd3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799552"
---
# <a name="pidlidinternetaccountstamp"></a>PidLidInternetAccountStamp

メッセージを配信するアカウントのアカウントのタイムスタンプを返します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidInetAcctStamp  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x00008581  <br/> |
|データを入力します。  <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、メッセージを配信しているアカウントについては、アカウント管理 API プロパティの[PROP_ACCT_STAMP](prop_acct_stamp.md)から返される値と同じ値を格納する必要があります。 
  
メッセージ ストア プロバイダーは、次のアクションが発生しないように、この名前付きプロパティと[PidLidInternetAccountName](pidlidinternetaccountname.md)を公開します。 
  
- ユーザーをクリックしたとき **[全員へ返信**電子メール メッセージ、Outlook は、アカウントに関連付けられており、返信の受信者のリストからのメッセージにスタンプがあるメール アドレスを削除します。 この現象は、この e メール アドレスが元のメッセージの送信者ではない場合、発生します。 
    
- 既定では、Outlook は、返信を送信し、元のメッセージの文字が印字されているアカウントを経由してメッセージを転送します。
    
通常、Outlook プロトコル マネージャーが、メッセージを提供し、Outlook がメッセージを配信しているアカウントを示すために**PidLidInternetAccountName**と**PidLidInternetAccountStamp**のプロパティを設定します。 ただし、メッセージ ストアは、トランスポートと密接に関連では、Outlook プロトコル マネージャーがメッセージを配信しませんし、Outlook は、これらのプロパティを設定できません。 このシナリオでは、Outlook は、 [IMAPIProp::GetIDsFromNames](http://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx)関数を呼び出します。 メッセージ ストア プロバイダーは、これらの名前付きプロパティを公開する必要がある場合は**IMAPIProp::GetIDsFromNames**を実装する必要があります、出力パラメーター *lppPropTags*をプロパティ タグを取得します。 Outlook は、これらのプロパティ タグを使用して、 [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx)メソッドを呼び出して、メッセージ ストア プロバイダーは、アカウント名と目的のアカウントのタイムスタンプを返すことができます。 
  
ストア プロバイダーでは、これらの名前のプロパティをサポートするには、 **IMAPIProp::GetIDsFromNames**を使用して、このプロパティのプロパティ タグを取得するように Outlook が予想されます。 Outlook では、 **IMAPIProp::GetIDsFromNames**の入力パラメーター *lppPropNames*が指す配列の一部として渡されるこの名前のプロパティに対応する[MAPINAMEID](http://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx)構造体の次の値を指定します。 
  
|||
|:-----|:-----|
|lpGuid。  <br/> |PSETID_Common  <br/> |
|ulKind。  <br/> |MNID_ID  <br/> |
|Kind.lID。  <br/> |dispidInetAcctStamp  <br/> |
   
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)
- [PidLidInternetAccountStamp の標準的なプロパティ](http://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)

