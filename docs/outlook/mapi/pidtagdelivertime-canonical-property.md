---
title: PidTagDeliverTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliverTime
api_type:
- HeaderDef
ms.assetid: da0ad17b-08ac-4c50-ac1d-13062b890dfd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 198e388f5cfb6ab0431e7b7a78b9a0be3d103597
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582120"
---
# <a name="pidtagdelivertime-canonical-property"></a>PidTagDeliverTime 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
元のメッセージが配信されたときの日時が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DELIVER_TIME  <br/> |
|識別子:  <br/> |0x0010  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|領域:  <br/> |MAPI の封筒  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、元のメッセージが配信レポートを生成しているメッセージング ユーザーに配信された時刻を示す配信レポートの受信者ごとのプロパティです。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

