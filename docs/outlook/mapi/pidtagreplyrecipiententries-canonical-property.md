---
title: PidTagReplyRecipientEntries 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagReplyRecipientEntries
api_type:
- COM
ms.assetid: a903fd22-a3f2-464f-99b0-c087e211b124
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b38207262fa97a368c8b993877c5694ed4c9d9be
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591613"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a>PidTagReplyRecipientEntries 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
返信を取得する受信者のエントリ識別子のサイズの配列を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_REPLY_RECIPIENT_ENTRIES  <br/> |
|識別子:  <br/> |0x004F  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI 封筒  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには [FLATENTRYLIST](flatentrylist.md) 構造体が含まれるので、複数値プロパティではありません。 
  
このプロパティが存在しない場合は、PR_SENDER_ENTRYID ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) プロパティによって **識別された** ユーザーにのみ返信が送信されます。 このプロパティと **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) プロパティが定義されている場合、この 2 つのプロパティで識別される受信者全員に返信が送信されます。 トランスポート プロバイダーは、これらのプロパティを使用して、通常の応答ロジックをオーバーライドします。
  
このプロパティまたは PR_REPLY_RECIPIENT_NAMES プロパティ **が** 設定されている場合は、他のプロパティも設定する必要があります。 これらのプロパティには同じ数の受信者が含まれている必要があります。また、それらのプロパティには同じ順序で含まれている必要があります。 これらの要件を満たさないと、予期しない結果が発生する可能性があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージで許容されるプロパティと操作を指定します。
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。
    
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

