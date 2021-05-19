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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ecfed5684ba2166c1c00c1fd07fa074b4ce9fd79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434075"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a>PidTagRequestedDeliveryMethod 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このプロパティには、メッセージ送信者の優先順に配信メソッド (サービス プロバイダー) のバイナリ配列が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_REQUESTED_DELIVERY_METHOD  <br/> |
|識別子:  <br/> |0x0C18  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 受信者  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティに含まれる配列は、各サービス プロバイダーの ASN.1 識別子で構成されます。
  
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

