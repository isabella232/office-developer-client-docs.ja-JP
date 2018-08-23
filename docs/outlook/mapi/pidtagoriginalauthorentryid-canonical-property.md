---
title: PidTagOriginalAuthorEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEntryId
api_type:
- COM
ms.assetid: 34654660-b003-42f5-9fcd-24ebaccd735d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 03dcc9a1f929bc6f99ca9e1dd9f75f3fb9c3dcb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562968"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a>PidTagOriginalAuthorEntryId 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
転送または返信する前にメッセージは、メッセージの最初のバージョンの作成者のエントリ id が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINAL_AUTHOR_ENTRYID  <br/> |
|識別子:  <br/> |0x004C  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、メッセージの作成者のアドレスのプロパティのいずれかです。 メッセージの最初の提出書類は、クライアント アプリケーションは、 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) の値にこのプロパティを設定する必要があります。 メッセージを転送または返信するときは変更されません。 
  
元の作成者プロパティは、ローカルのメッセージング ドメインの外部からの情報の保持に使用できます。 このプロパティがその元の情報を保証する手段を提供する、インターネットからなど、別のメッセージング ドメインからメッセージが着信するときは、失われていません。
  
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

