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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 09331e1201b6f6e45bb9e26e618ee59e67efbf8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409581"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a>PidTagOriginalAuthorSearchKey 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの最初のバージョンの作成者の検索キー(転送または返信前のメッセージ)が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINAL_AUTHOR_SEARCH_KEY  <br/> |
|識別子:  <br/> |0x0056  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、メッセージの作成者のアドレス プロパティの 1 つです。 メッセージの最初の送信時に、クライアント アプリケーションは [PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)プロパティの値に **このプロパティPR_SENDER_SEARCH_KEY** 設定する必要があります。 メッセージが転送または返信された場合は、変更されません。 
  
元の作成者プロパティを使用すると、ローカル メッセージング ドメイン外からの情報を保持できます。 インターネットなどの別のメッセージング ドメインからメッセージが到着すると、これらのプロパティを使用して、元の情報が失われなかねない方法が提供されます。
  
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

