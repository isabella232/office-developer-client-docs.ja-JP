---
title: PidTagIpmSentMailEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagIpmSentMailEntryId
api_type:
- HeaderDef
ms.assetid: f6877435-6b26-4060-924f-a65591ad9538
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0efc6ede87caad5f6ac3b3374d23da9219967f90
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599946"
---
# <a name="pidtagipmsentmailentryid-canonical-property"></a>PidTagIpmSentMailEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
標準の対人メッセージ (IPM) 送信アイテム フォルダーのエントリ識別子を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_IPM_SENTMAIL_ENTRYID  <br/> |
|識別子:  <br/> |0x35E4  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |フォルダー  <br/> |
   
## <a name="remarks"></a>注釈

送信後、対人メッセージは通常、[送信されたアイテム] フォルダーに配置されます。 クライアントは、このプロパティを使用して、送信 **PR_SENTMAIL_ENTRYIDのプロパティ** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティを設定できます。 
  
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

