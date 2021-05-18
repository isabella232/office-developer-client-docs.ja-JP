---
title: PidTagFreeBusyPublishEnd 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyPublishEnd
api_type:
- HeaderDef
ms.assetid: df239741-6a63-4cd4-9bbb-42c0f5c668a5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3b4a8cb7136eee914dc697d24e0374ccb4b6f8b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316185"
---
# <a name="pidtagfreebusypublishend-canonical-property"></a>PidTagFreeBusyPublishEnd 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
発行範囲の終了時刻を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_FREEBUSY_PUBLISH_END  <br/> |
|識別子:  <br/> |0x6848  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |空き時間情報  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの値は、発行範囲の開始日に **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) の値を追加して計算されます。 この値は、協定世界時 (UTC) で 1601 年 1 月 1 日午前 0 時以降の分数で表されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> ユーザーまたはリソースの可用性を公開します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

