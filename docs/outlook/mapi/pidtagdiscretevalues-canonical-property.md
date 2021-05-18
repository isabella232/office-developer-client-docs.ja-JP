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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6d6974302e3413db3590abbbd3e6567976c6ac72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404842"
---
# <a name="pidtagdiscretevalues-canonical-property"></a>PidTagDiscreteValues 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
配信以外のレポートがリスト全体ではなく配布リストの個別のメンバーにのみ適用される場合は TRUE を含む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DISCRETE_VALUES  <br/> |
|識別子:  <br/> |0x0E0E  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |MAPI 送信不可  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、配布リストの 1 つ以上のメンバーにメッセージを配信できない場合に、配信以外のレポート内で使用されます。 その目的は、再送信の試行を、配布リスト全体ではなく、個々のメンバーにのみ制限する目的です。 
  
配信されないレポートの受信者テーブルには、メッセージを配信できないすべての受信者のエントリと、メッセージが属する配布リスト (その場合) のエントリが含まれる。 トランスポート プロバイダーは、配布リスト エントリごとにこのプロパティを TRUE に設定する必要があります。 配布リストから **PR_DISPLAY_NAME** [(PidTagDisplayName)、PR_ENTRYID](pidtagdisplayname-canonical-property.md)[(PidTagEntryId)、](pidtagentryid-canonical-property.md)および **PR_SEARCH_KEY** ([PidTagSearchKey)](pidtagsearchkey-canonical-property.md)を配布リストから **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName)](pidtagoriginaldisplayname-canonical-property.md) **、PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId)、](pidtagoriginalentryid-canonical-property.md)および PR_ORIGINAL_SEARCH_KEY **(** [PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) プロパティをその配布リストの各メンバーにコピーする必要があります。  
  
 **PR_DISCRETE_VALUES、** 配布リスト以外の配信レポート受信者エントリに対して設定する必要があります。 
  
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

