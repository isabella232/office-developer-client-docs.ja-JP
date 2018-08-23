---
title: PidTagRequestedDeliveryMethod 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRequestedDeliveryMethod
api_type:
- COM
ms.assetid: cc55089b-e389-405e-8174-f5b5ec352f78
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f18d726c1b06a6fb7f79964165bbdb9074a6d4d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571368"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a>PidTagRequestedDeliveryMethod 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
このプロパティには、メッセージの送信元の優先順位に従って指定の配送方法 (サービス プロバイダー) のバイナリの配列が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_REQUESTED_DELIVERY_METHOD  <br/> |
|識別子:  <br/> |0x0C18  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI 受信者  <br/> |
   
## <a name="remarks"></a>注釈

このに含まれている配列の各サービス プロバイダーの ASN.1 識別子のプロパティで構成されます。
  
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

