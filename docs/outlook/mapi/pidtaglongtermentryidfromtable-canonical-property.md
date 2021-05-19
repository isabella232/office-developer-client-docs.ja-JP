---
title: PidTagLongTermEntryIdFromTable 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLongTermEntryIdFromTable
api_type:
- HeaderDef
ms.assetid: d9457fea-4b1e-4cf6-9c4b-14c98fbec2a1
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 574c7d305f105709aebcd41e30b034fbac1892a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425667"
---
# <a name="pidtaglongtermentryidfromtable-canonical-property"></a>PidTagLongTermEntryIdFromTable 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アイテムの長期エントリ識別子を取得します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_LONGTERM_ENTRYID_FROM_TABLE  <br/> |
|識別子:  <br/> |0x6670  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Table プロパティ  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、コンテンツ テーブルで使用して、短期的なエントリ識別子の代わりに、アイテムのエントリ識別子を長期エントリ識別子として取得できます。 長期識別子と短期識別子の詳細については、「PR_ENTRYID **(** [PidTagEntryId)」を参照してください](pidtagentryid-canonical-property.md)。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagEntryId 標準プロパティ](pidtagentryid-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

