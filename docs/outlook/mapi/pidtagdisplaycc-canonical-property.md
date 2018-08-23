---
title: PidTagDisplayCc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayCc
api_type:
- HeaderDef
ms.assetid: 00377e78-a208-4942-a7a6-893b2a71ab0b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6257557a8848c1abbaf8ceb15f719c50e4fec8c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802701"
---
# <a name="pidtagdisplaycc-canonical-property"></a>PidTagDisplayCc 標準プロパティ

  
  
**適用対象**: Outlook 
  
ASCII のリスト セミコロン (;)、カーボン コピー (CC) メッセージの受信者の表示名にはが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DISPLAY_CC、PR_DISPLAY_CC_A、PR_DISPLAY_CC_W  <br/> |
|識別子:  <br/> |0x0E03  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |Message  <br/> |
   
## <a name="remarks"></a>注釈

メッセージ ・ ストアは、 [IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドを使用して、メッセージ オブジェクトに対してこれらのプロパティを計算します。 メッセージ ・ ストアは、常に最後に保存されているメッセージの状態を反映するようにもこれらのプロパティを管理します。 値は、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)へのすべての呼び出しの時点で同期されます。 
  
カーボン コピー受信者、メッセージがない場合は、メッセージ ・ ストアは S_OK とこれらのプロパティに空の文字列の戻り値を持つ、 [IMAPIProp::GetProps](imapiprop-getprops.md)の呼び出しに応答します。 
  
ローカライズ可能な必要が、あるは、MAPI は、すべての受信者の名前のこれらのガイドラインを提供します。
  
- すべての名前をローカライズすることがあります。 
    
- **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))、 **PR_DISPLAY_CC**、およびプロパティの**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) の名を区切るために使用される文字にセミコロンがあります。 MAPI 受信者の名前にセミコロンを使用することはできません。 
    
- クライアントは、ユーザー インターフェイスでプロパティ情報を表示する前にこのプロパティのローカライズされた区切り記号で発生した各セミコロンを付ける必要があります。 
    
- メッセージを転送するには、クライアントでは、カーボン コピー受信者行の区切り文字に変換する必要はありません。 
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
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

