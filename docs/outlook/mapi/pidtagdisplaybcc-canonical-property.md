---
title: PidTagDisplayBcc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayBcc
api_type:
- HeaderDef
ms.assetid: ab5bcd67-d54e-46e9-b94e-a652aac3e81c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 74669d102462e1a825568615d1d30346e99e90a6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388260"
---
# <a name="pidtagdisplaybcc-canonical-property"></a>PidTagDisplayBcc 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ASCII のリスト セミコロン (;)、ブラインド カーボン コピー (BCC) メッセージの受信者の表示名にはが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DISPLAY_BCC、PR_DISPLAY_BCC_A、PR_DISPLAY_BCC_W  <br/> |
|識別子:  <br/> |0x0E02  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |Message  <br/> |
   
## <a name="remarks"></a>備考

メッセージ ・ ストアは、 [IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドを使用して、メッセージ オブジェクトに対してこれらのプロパティを計算します。 メッセージ ・ ストアは、常に最後に保存されているメッセージの状態を反映するようにもこれらのプロパティを管理します。 値は、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドの呼び出しごとの時間に同期されます。 
  
ブラインド カーボン コピー受信者、メッセージがない場合は、S_OK と空の文字列の戻り値を持つ[IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出す**PR_DISPLAY_BCC**のメッセージ ・ ストアの応答です。 
  
ローカライズ可能な必要が、あるは、MAPI は、すべての受信者の名前のこれらのガイドラインを提供します。
  
- すべての名前をローカライズすることがあります。 
    
- **PR_DISPLAY_BCC**、 **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))、およびプロパティの**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) の名を区切るために使用される文字にセミコロンがあります。 MAPI 受信者の名前にセミコロンを使用することはできません。 
    
- クライアントは、ユーザー インターフェイスでプロパティ情報を表示する前にこのプロパティのローカライズされた区切り記号で発生した各セミコロンを付ける必要があります。 
    
- メッセージを転送するには、クライアントでは、ブラインド カーボン コピー受信者行の区切り文字に変換する必要はありません。 
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> クライアント上のフォルダーを共有に関連する情報の送信に使用されるメッセージの形式について説明します。
    
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

