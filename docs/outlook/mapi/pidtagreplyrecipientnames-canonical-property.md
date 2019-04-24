---
title: PidTagReplyRecipientNames 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientNames
api_type:
- COM
ms.assetid: f5ae6124-3e44-400f-95c2-24b19f3085b5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 02dcbcccd003fb0b53356da11a3b90b38e632c2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355175"
---
# <a name="pidtagreplyrecipientnames-canonical-property"></a>PidTagReplyRecipientNames 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
応答を取得する受信者の表示名の一覧が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_REPLY_RECIPIENT_NAMES、PR_REPLY_RECIPIENT_NAMES_A、PR_REPLY_RECIPIENT_NAMES_W  <br/> |
|識別子:  <br/> |0x0050  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI エンベロープ  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティには、セミコロンで区切られた表示名が含まれています。
  
このプロパティが存在しない場合、返信は**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) プロパティによって識別されるユーザーにのみ送信されます。 **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) とこれらのプロパティが定義されている場合、返信は、これら2つのプロパティによって識別されるすべての受信者に送信されます。 トランスポートプロバイダーは、これらのプロパティを使用して、通常の応答ロジックを上書きします。
  
**PR_REPLY_RECIPIENT_ENTRIES**またはこれらのプロパティのいずれかが設定されている場合は、もう一方のプロパティも設定する必要があります。 これらのプロパティには、同じ数の受信者が含まれている必要があります。また、これらのプロパティは同じ順序で格納されている必要があります。 これらの要件を遵守できないと、予期しない結果になることがあります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージに対して許容されるプロパティと操作を指定します。
    
[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

