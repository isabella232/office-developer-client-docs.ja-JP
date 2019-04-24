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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360817"
---
# <a name="pidtagdisplaybcc-canonical-property"></a>PidTagDisplayBcc 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
bcc (ブラインドカーボンコピー) メッセージ受信者の表示名の ASCII リストをセミコロン (;) で区切って記述します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DISPLAY_BCC、PR_DISPLAY_BCC_A、PR_DISPLAY_BCC_W  <br/> |
|識別子:  <br/> |0x0e02  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メッセージ  <br/> |
   
## <a name="remarks"></a>解説

メッセージストアは、 [IMessage:: modifyrecipients](imessage-modifyrecipients.md)メソッドを使用して、これらのプロパティをメッセージオブジェクトで計算します。 また、メッセージストアは、メッセージの最後に保存された状態を常に反映するようにこれらのプロパティを保持します。 値は、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出すたびに同期されます。 
  
メッセージにブラインドカーボンコピー受信者が含まれていない場合、メッセージストアは、戻り値が S_OK で、 **PR_DISPLAY_BCC**用の空の文字列である[imapiprop:: GetProps](imapiprop-getprops.md)呼び出しに応答する必要があります。 
  
ローカライズが必要になる可能性があるため、MAPI では、すべての受信者名について次のガイドラインが提供されています。
  
- すべての名前をローカライズできるようにする必要があります。 
    
- セミコロンは、 **PR_DISPLAY_BCC**、 **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))、 **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) の各プロパティで名前を区切るために使用される文字である必要があります。 MAPI では、受信者名の中にセミコロンを使用することはできません。 
    
- クライアントは、ユーザーインターフェイスにプロパティ情報が表示されるようにするために、このプロパティで検出された各セミコロンをローカライズされた区切り文字に変換する必要があります。 
    
- メッセージを転送する場合、クライアントはブラインドカーボンコピー受信者行の区切り文字を変換する必要はありません。 
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> クライアント上の共有フォルダーに関連する情報を送信するために使用されるメッセージの形式について説明します。
    
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

