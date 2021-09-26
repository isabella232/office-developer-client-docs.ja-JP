---
title: PidTagOriginallyIntendedRecipEmailAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginallyIntendedRecipEmailAddress
api_type:
- COM
ms.assetid: 6a85b695-731a-4401-9c9c-fda6bc308558
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d95ab4a6ca8d07b7df28af2afed089ec160a0ed6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583303"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a>PidTagOriginallyIntendedRecipEmailAddress 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
自動送信されたメッセージの最初に意図した受信者の電子メール アドレスを格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS、PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A、PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W  <br/> |
|識別子:  <br/> |0x007C  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |サーバー  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、最初に意図したメッセージ受信者のアドレス プロパティの例です。 メッセージを転送した自動エージェントによって設定する必要があります。
  
これらのプロパティは、受信者ごとの X.400 レポート属性に対応します。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

