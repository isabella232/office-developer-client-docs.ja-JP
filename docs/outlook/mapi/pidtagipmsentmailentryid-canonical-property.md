---
title: PidTagIpmSentMailEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmSentMailEntryId
api_type:
- HeaderDef
ms.assetid: f6877435-6b26-4060-924f-a65591ad9538
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ee2e9e7f73e03e0a201a5ff41ea6e37a78c668a1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569576"
---
# <a name="pidtagipmsentmailentryid-canonical-property"></a>PidTagIpmSentMailEntryId 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
標準的な個人間メッセージ (IPM) の [送信済みアイテム フォルダーのエントリ id が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_IPM_SENTMAIL_ENTRYID  <br/> |
|識別子:  <br/> |0x35E4  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>注釈

、送信した個人間のメッセージは通常、送信済みアイテム フォルダーに配置されます。 クライアントは、送信されたメッセージの**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) のプロパティを設定するのにはこのプロパティを使用できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

