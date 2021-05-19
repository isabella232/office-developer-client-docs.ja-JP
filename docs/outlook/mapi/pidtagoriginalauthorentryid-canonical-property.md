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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 866c28bc08f669d18487c99c9a13bc7347b605fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425590"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a>PidTagOriginalAuthorEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの最初のバージョンの作成者 (転送または返信前のメッセージ) のエントリ識別子を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINAL_AUTHOR_ENTRYID  <br/> |
|識別子:  <br/> |0x004C  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、メッセージの作成者のアドレス プロパティの 1 つです。 メッセージの最初の送信時に、クライアント アプリケーションは、このプロパティを PR_SENDER_ENTRYID  ([PidTagSenderEntryId)](pidtagsenderentryid-canonical-property.md)の値に設定する必要があります。 メッセージが転送または返信された場合は、変更されません。 
  
元の author プロパティを使用すると、ローカル メッセージング ドメインの外部からの情報を保持できます。 インターネットなど、別のメッセージング ドメインからメッセージが届いた場合、このプロパティは元の情報が失われなかねない方法を提供します。
  
## <a name="related-resources"></a>関連リソース

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

