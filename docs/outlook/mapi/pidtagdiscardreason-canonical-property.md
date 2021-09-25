---
title: PidTagDiscardReason 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDiscardReason
api_type:
- HeaderDef
ms.assetid: 5004dc1f-6bd3-4764-b83c-d04d83161dba
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3b84d43c4653c10f8120e77aa98cc68eed3bf545
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600191"
---
# <a name="pidtagdiscardreason-canonical-property"></a>PidTagDiscardReason 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ転送エージェント (MTA) がメッセージを破棄した理由が含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DISCARD_REASON  <br/> |
|識別子:  <br/> |0x0011  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 封筒  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティに含まれる理由は、メッセージの非送信レポートで使用されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagNonDeliveryReportReasonCode 標準プロパティ](pidtagnondeliveryreportreasoncode-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

