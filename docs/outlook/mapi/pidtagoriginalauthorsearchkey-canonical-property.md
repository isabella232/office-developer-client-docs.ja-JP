---
title: PidTagOriginalAuthorSearchKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorSearchKey
api_type:
- COM
ms.assetid: 4a10cf99-c5e6-4a24-b531-3aebb7800bfe
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 09331e1201b6f6e45bb9e26e618ee59e67efbf8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356260"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a>PidTagOriginalAuthorSearchKey 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
最初のバージョンのメッセージ、つまり転送または返信する前のメッセージの作成者の検索キーが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINAL_AUTHOR_SEARCH_KEY  <br/> |
|識別子:  <br/> |0x0056  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |サーバー  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、メッセージの作成者のアドレスプロパティの1つです。 クライアントアプリケーションでは、最初にメッセージを送信するときに、このプロパティを**PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)プロパティの値に設定する必要があります。 メッセージが転送または返信されるときには変更されません。 
  
元の作成者のプロパティを使用すると、ローカルのメッセージングドメインの外部にある情報を保持できます。 インターネットからなど、他のメッセージングドメインからメッセージが到着すると、これらのプロパティを使用して元の情報が失われないようにすることができます。
  
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

