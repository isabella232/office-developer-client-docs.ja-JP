---
title: PidTagDisplayTo 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDisplayTo
api_type:
- HeaderDef
ms.assetid: 700cc03b-5d98-40ce-adb5-a11fdac8aa28
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: db57364669ecd35d3e2944563735ca2417cf36c1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579097"
---
# <a name="pidtagdisplayto-canonical-property"></a>PidTagDisplayTo 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プライマリ (宛先) メッセージ受信者の表示名の一覧をセミコロン (;)) で区切;)。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DISPLAY_TO、PR_DISPLAY_TO_A、PR_DISPLAY_TO_W  <br/> |
|識別子:  <br/> |0x0E04  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メッセージ  <br/> |
   
## <a name="remarks"></a>注釈

メッセージ ストアは [、IMessage::ModifyRecipients](imessage-modifyrecipients.md) メソッドを使用して、メッセージ オブジェクトのこれらのプロパティを計算します。 また、メッセージ ストアは、メッセージの最後に保存された状態を常に反映するように、これらのプロパティを保持します。 値は [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出すごとに同期されます。 
  
メッセージにプライマリ受信者がない場合、メッセージ ストアは、S_OK の戻り値と PR_DISPLAY_TO の空の文字列を持つ [IMAPIProp::GetProps](imapiprop-getprops.md) 呼び出し **に応答する必要があります**。 
  
ローカライズの必要性が考えられるため、MAPI には、すべての受信者名に関する次のガイドラインが記載されています。
  
- すべての名前をローカライズできる必要があります。 
    
- **セミコロンは、PR_DISPLAY_BCC** ([PidTagDisplayBcc)](pidtagdisplaybcc-canonical-property.md) **、PR_DISPLAY_CC** ([PidTagDisplayCc)、](pidtagdisplaycc-canonical-property.md)および PR_DISPLAY_TO プロパティの名前を区切る **文字である必要** があります。 MAPI では、受信者名内でセミコロンを使用することはできません。 
    
- クライアントは、ユーザー インターフェイスに情報を表示する前に、PR_DISPLAY_TO および関連するプロパティで検出された各セミコロンをローカライズされた区切り文字に変換する必要があります。 
    
- メッセージを転送する場合、クライアントはプライマリ受信者行の区切り文字を変換する必要があります。 
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
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

