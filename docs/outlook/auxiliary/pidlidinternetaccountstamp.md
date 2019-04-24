---
title: PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 52003a4e-1b61-2965-5204-6601652dd15b
description: メッセージを配信したアカウントのアカウントスタンプを返します。
ms.openlocfilehash: c5da45268cefbe09588fdcfcda32e4e7a4be9d5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327728"
---
# <a name="pidlidinternetaccountstamp"></a>PidLidInternetAccountStamp

メッセージを配信したアカウントのアカウントスタンプを返します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidinetacctstamp  <br/> |
|プロパティセット:  <br/> |PSETID_Common  <br/> |
|ロング ID (LID):  <br/> |0x00008581  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>解説

このプロパティには、メッセージを配信したアカウントのアカウント管理 API プロパティ[PROP_ACCT_STAMP](prop_acct_stamp.md)から返されるものと同じ値が含まれている必要があります。 
  
メッセージストアプロバイダーは、この名前付きプロパティと[PidLidInternetAccountName](pidlidinternetaccountname.md)を公開して、次のアクションが実行されるようにします。 
  
- ユーザーが電子メールメッセージで [**全員へ返信**] をクリックすると、Outlook はそのアカウントに関連付けられている電子メールアドレスを削除し、返信の受信者リストからメッセージにスタンプされます。 この動作は、この電子メールアドレスが元のメッセージの送信者ではない場合に発生します。 
    
- 既定では、Outlook は、元のメッセージにスタンプされているアカウントを使用して、返信メッセージと転送メッセージを送信します。
    
通常、outlook プロトコルマネージャーはメッセージを配信し、outlook は**PidLidInternetAccountName**および**PidLidInternetAccountStamp**プロパティを設定して、メッセージを配信したアカウントを示します。 ただし、メッセージストアがトランスポートと密に結合されている場合、outlook プロトコルマネージャーはメッセージを配信しないため、outlook はこれらのプロパティを設定できません。 このシナリオでは、Outlook は[imapiprop:: getidsfromnames](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx)関数を呼び出します。 メッセージストアプロバイダーがこれらの名前付きプロパティを公開する場合は、出力パラメーター *lppproptags*を使用して**imapiprop:: getidsfromnames**を実装し、プロパティタグを返す必要があります。 その後、Outlook は、これらのプロパティタグを使用して[imapiprop:: GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx)メソッドを呼び出すことができ、メッセージストアプロバイダーは必要なアカウントのアカウント名とスタンプを返すことができます。 
  
このような名前付きプロパティをサポートするには、ストアプロバイダーが**imapiprop:: getidsfromnames**を使用して、このプロパティのプロパティタグを取得する必要があります。 Outlook では、この名前付きプロパティに対応する[mapinameid](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx)構造体の次の値が指定されています。この名前は、入力パラメーター *lpppropnames の名前*によって示される配列の一部として渡されます。 **** 
  
|||
|:-----|:-----|
|lpguid:  <br/> |PSETID_Common  <br/> |
|ulkind:  <br/> |MNID_ID  <br/> |
|ふたの種類:  <br/> |dispidinetacctstamp  <br/> |
   
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)
- [PidLidInternetAccountStamp 標準プロパティ](https://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)

