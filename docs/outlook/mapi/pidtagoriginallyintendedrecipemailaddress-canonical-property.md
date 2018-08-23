---
title: PidTagOriginallyIntendedRecipEmailAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEmailAddress
api_type:
- COM
ms.assetid: 6a85b695-731a-4401-9c9c-fda6bc308558
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f4adbdfc041ebe5213c384db98343baa82af5b05
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572726"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a>PidTagOriginallyIntendedRecipEmailAddress 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
自動転送されたメッセージの最初の目的の受信者の電子メール アドレスが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS、PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A、PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W  <br/> |
|識別子:  <br/> |0x007C  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティでは、本来意図されているメッセージの受信者のアドレスのプロパティの例を示します。 メッセージを転送するには自動エージェントが設定されなければなりません。
  
これらのプロパティは、レポートの X.400 受信者ごとの属性に対応します。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

