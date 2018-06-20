---
title: PidTagReplyRecipientEntries の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientEntries
api_type:
- COM
ms.assetid: a903fd22-a3f2-464f-99b0-c087e211b124
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1ab8828dd2fc28a2fba1620fc251ba0a87c3e2bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803330"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a>PidTagReplyRecipientEntries の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
応答を取得するのには受信者のエントリ id のサイズの配列が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_REPLY_RECIPIENT_ENTRIES  <br/> |
|識別子:  <br/> |0x004F  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI の封筒  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、 [FLATENTRYLIST](flatentrylist.md)構造体を格納し、複数値を持つプロパティではありません。 
  
このプロパティが存在しない場合は、 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) のプロパティで指定されたユーザーのみに返信が送信されます。 これと**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) のプロパティが定義されている場合、これら 2 つのプロパティで識別される受信者全員に返信が送信されます。 トランスポート プロバイダーは、通常の応答のロジックをオーバーライドするのには、これらのプロパティを使用します。
  
このプロパティまたは**PR_REPLY_RECIPIENT_NAMES**プロパティが設定されている場合も、他のプロパティを設定しなければなりません。 これらのプロパティは、同じ数の受信者を含める必要があり、同じ順序でそれらに含まれる必要があります。 これらの要件を遵守すると、可能性が予期しない結果です。 
  
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
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

