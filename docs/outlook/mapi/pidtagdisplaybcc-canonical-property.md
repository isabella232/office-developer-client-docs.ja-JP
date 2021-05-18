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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 74669d102462e1a825568615d1d30346e99e90a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360817"
---
# <a name="pidtagdisplaybcc-canonical-property"></a>PidTagDisplayBcc 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ブラインド カーボン コピー (BCC) メッセージ受信者の表示名の ASCII リストをセミコロン (;)) で区切って含;)。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DISPLAY_BCC、PR_DISPLAY_BCC_A、PR_DISPLAY_BCC_W  <br/> |
|識別子:  <br/> |0x0E02  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メッセージ  <br/> |
   
## <a name="remarks"></a>注釈

メッセージ ストアは [、IMessage::ModifyRecipients](imessage-modifyrecipients.md) メソッドを使用して、メッセージ オブジェクトのこれらのプロパティを計算します。 また、メッセージ ストアは、メッセージの最後に保存された状態を常に反映するように、これらのプロパティを保持します。 値は [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出すごとに同期されます。 
  
メッセージにブラインド カーボン コピー受信者がない場合、メッセージ ストアは、S_OK の戻り値と PR_DISPLAY_BCC の空の文字列を持つ [IMAPIProp::GetProps](imapiprop-getprops.md) 呼び **出しに応答する必要があります**。 
  
ローカライズの必要性が考えられるため、MAPI には、すべての受信者名に関する次のガイドラインが記載されています。
  
- すべての名前をローカライズできる必要があります。 
    
- **セミコロンは、PR_DISPLAY_BCC 、PR_DISPLAY_CC**([PidTagDisplayCc)](pidtagdisplaycc-canonical-property.md)プロパティ、およびPR_DISPLAY_TO **(** [PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) プロパティの名前を区切る文字である必要があります。 MAPI では、受信者名内でセミコロンを使用することはできません。 
    
- クライアントは、ユーザー インターフェイスでプロパティ情報を表示する前に、このプロパティで検出された各セミコロンをローカライズされた区切り文字に変換する必要があります。 
    
- メッセージを転送する場合、クライアントはブラインド カーボン コピー受信者行の区切り文字を変換する必要があります。 
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> クライアント上の共有フォルダーに関連する情報を送信するために使用されるメッセージの形式について説明します。
    
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

