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
ms.openlocfilehash: fc9a64abefb9a4acaa9a1da396fb27f897f04ec2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585606"
---
# <a name="pidtagreplyrecipientnames-canonical-property"></a>PidTagReplyRecipientNames 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
応答を取得するのには受信者の表示名の一覧が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_REPLY_RECIPIENT_NAMES、PR_REPLY_RECIPIENT_NAMES_A、PR_REPLY_RECIPIENT_NAMES_W  <br/> |
|識別子:  <br/> |0x0050  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |MAPI の封筒  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティには、セミコロンで区切られた表示名が含まれています。
  
このプロパティが存在しない場合は、返信は**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) のプロパティで指定されたユーザーにのみ送信されます。 **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) とこれらのプロパティが定義されている場合、これら 2 つのプロパティで識別される受信者全員に返信が送信されます。 トランスポート プロバイダーは、通常の応答のロジックをオーバーライドするのには、これらのプロパティを使用します。
  
**PR_REPLY_RECIPIENT_ENTRIES**またはこれらのプロパティのいずれかが設定されている場合も、他のプロパティを設定しなければなりません。 これらのプロパティは、同じ数の受信者を含める必要があり、同じ順序でそれらに含まれる必要があります。 これらの要件を遵守すると、可能性が予期しない結果です。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージの許可の操作を指定します。
    
[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。
    
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

