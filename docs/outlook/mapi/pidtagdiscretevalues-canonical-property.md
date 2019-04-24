---
title: PidTagDiscreteValues 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDiscreteValues
api_type:
- HeaderDef
ms.assetid: 958f3cf7-953a-43f4-9102-ad35edf5e813
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6d6974302e3413db3590abbbd3e6567976c6ac72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360824"
---
# <a name="pidtagdiscretevalues-canonical-property"></a>PidTagDiscreteValues 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
リスト全体ではなく、配布リストの個々のメンバーにのみ配信不能レポートが適用される場合は、TRUE が含まれます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DISCRETE_VALUES  <br/> |
|識別子:  <br/> |0x0e0e  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |MAPI ノンノンアウトテーブル  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、メッセージが配布リストの1つ以上のメンバーに配信できなかった場合に、配信不能レポート内で使用されます。 この目的は、再送信の試行を、配布リスト全体ではなく、個々のメンバーのみに制限することです。 
  
配信不能レポートの recipient テーブルには、そのメッセージが配信できなかったすべての受信者のエントリと、それが属する配布リスト (存在する場合) のエントリが含まれています。 トランスポートプロバイダーは、各配布リストエントリに対してこのプロパティを TRUE に設定し、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、および**PR_SEARCH_KEY**をコピーする必要があります ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) を配布リストから**PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md))、 **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md))、および**PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) プロパティを使用して、配布リストのメンバーを指定します。 
  
 配布リスト以外の配信不能レポート受信者エントリに対して**PR_DISCRETE_VALUES**を設定することはできません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

