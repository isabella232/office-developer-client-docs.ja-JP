---
title: PidTagDiscardReason 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDiscardReason
api_type:
- HeaderDef
ms.assetid: 5004dc1f-6bd3-4764-b83c-d04d83161dba
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 32c81474580dbe4948c40390dadd0445776ab825
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360845"
---
# <a name="pidtagdiscardreason-canonical-property"></a>PidTagDiscardReason 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ転送エージェント (MTA) がメッセージを破棄した理由が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DISCARD_REASON  <br/> |
|識別子:  <br/> |0x0011  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI エンベロープ  <br/> |
   
## <a name="remarks"></a>解説

このプロパティに含まれている理由は、メッセージの配信不能レポートで使用されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagNonDeliveryReportReasonCode 標準プロパティ](pidtagnondeliveryreportreasoncode-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

