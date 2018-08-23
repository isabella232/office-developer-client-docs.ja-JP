---
title: PidTagDisplayTo 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTo
api_type:
- HeaderDef
ms.assetid: 700cc03b-5d98-40ce-adb5-a11fdac8aa28
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 79a0307aaf8b91a50485234acc2e1cbdd2314b47
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574168"
---
# <a name="pidtagdisplayto-canonical-property"></a>PidTagDisplayTo 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
プライマリ (する、セミコロン (;)、メッセージの受信者) の表示名の一覧が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DISPLAY_TO、PR_DISPLAY_TO_A、PR_DISPLAY_TO_W  <br/> |
|識別子:  <br/> |0x0E04  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |Message  <br/> |
   
## <a name="remarks"></a>注釈

メッセージ ・ ストアは、 [IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドを使用して、メッセージ オブジェクトに対してこれらのプロパティを計算します。 メッセージ ・ ストアは、常に最後に保存されているメッセージの状態を反映するようにもこれらのプロパティを管理します。 値は、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドの呼び出しごとの時間に同期されます。 
  
プライマリ受信者、メッセージがない場合は、メッセージ ・ ストア応答、 [IMAPIProp::GetProps](imapiprop-getprops.md)呼び出しの戻り値が S_OK と空の文字列の**PR_DISPLAY_TO**にします。 
  
ローカライズ可能な必要が、あるは、MAPI は、すべての受信者の名前のこれらのガイドラインを提供します。
  
- すべての名前をローカライズすることがあります。 
    
- セミコロンで**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))、 **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))、およびプロパティの**PR_DISPLAY_TO**名を区切るために使用される文字があります。 MAPI 受信者の名前にセミコロンを使用することはできません。 
    
- クライアントで発生した各セミコロンを付ける必要があります**PR_DISPLAY_TO**とユーザー ・ インタ フェースの情報を表示する前にローカライズされた区切り記号に関連するプロパティ。 
    
- メッセージを転送するには、クライアントでは、プライマリ受信者行の区切り文字に変換する必要はありません。 
    
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

