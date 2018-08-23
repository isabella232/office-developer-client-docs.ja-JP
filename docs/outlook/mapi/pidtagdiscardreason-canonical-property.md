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
ms.openlocfilehash: a8835b7234a209d5cb80a19593632380f6d83826
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593159"
---
# <a name="pidtagdiscardreason-canonical-property"></a>PidTagDiscardReason 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ転送エージェント (MTA) がメッセージを破棄する理由の理由が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DISCARD_REASON  <br/> |
|識別子:  <br/> |0x0011  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI の封筒  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティに含まれている理由は、メッセージの配信不能レポートで使用されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagNonDeliveryReportReasonCode 標準プロパティ](pidtagnondeliveryreportreasoncode-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

