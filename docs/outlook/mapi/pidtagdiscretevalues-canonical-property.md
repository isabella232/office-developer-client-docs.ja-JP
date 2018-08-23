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
ms.openlocfilehash: f1aa54c3364185d322137ef41f6aface31c5c556
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587419"
---
# <a name="pidtagdiscretevalues-canonical-property"></a>PidTagDiscreteValues 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
配信不能レポートは、リスト全体ではなく、配布リストのみを個別のメンバーを適用する場合は TRUE が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DISCRETE_VALUES  <br/> |
|識別子:  <br/> |0x0E0E  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |MAPI 以外から送信できます。  <br/> |
   
## <a name="remarks"></a>注釈

配布リストの 1 つまたは複数のメンバーにメッセージを配信できませんでしたと、配信不能レポート内でこのプロパティが使用されます。 その目的は、再送信を制限しようとすると個々 のメンバーだけと、配布リストではなく、全体としてです。 
  
配信不能レポートの受信者テーブルが含まれていますエントリにはユーザーのメッセージ配信できませんでした、すべての受信者および配布リストで、該当する場合、所属しています。 トランスポート プロバイダーは、各配布リストのエントリの場合は TRUE にこのプロパティを設定する必要があり。、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) および**PR_SEARCH_KEY** ([をコピーする必要があります。PidTagSearchKey](pidtagsearchkey-canonical-property.md)) **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md))、 **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) および**PR_ORIGINAL_SEARCH_KEY** ([の配布リストからPidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) その配布リストの各メンバーのプロパティです。 
  
 配信不能レポートの受信者のエントリ、配布リスト以外の**PR_DISCRETE_VALUES**を設定しないでください。 
  
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

