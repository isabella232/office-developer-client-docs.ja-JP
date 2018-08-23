---
title: PidTagMessageCcMe 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageCcMe
api_type:
- HeaderDef
ms.assetid: 7310a0f2-a109-40a4-99bf-e963d754a067
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 82d043adfe6e480b4d490f44ad89d73535c80c9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569779"
---
# <a name="pidtagmessageccme-canonical-property"></a>PidTagMessageCcMe 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
このメッセージングのユーザーを選択し、具体的にはこのメッセージのカーボン コピー (CC) 受信者という配布リストの一部ではない場合、TRUE が格納されます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MESSAGE_CC_ME  <br/> |
|識別子:  <br/> |0x0058  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティを確認するかどうかユーザー名に明示的にカーボン コピー受信者一覧で、リスト内のすべてのエントリを検査せずに便利な方法を提供します。 
  
このプロパティは、受信したメッセージの受信確認の時点での自動処理を支援します。 トランスポート プロバイダーのオプションでは、このプロパティは FALSE が含まれて か、またはメッセージングのユーザーが受信者テーブルに直接表示されていない場合に設定されていません。 
  
配布リストの展開またはブラインド カーボン コピーの指定によるメッセージの配信は、このプロパティを設定するには発生しません。 受信者は明示的に指定する必要があります。 
  
一般に、未送信のメッセージには**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) または**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) は、このプロパティ設定しません。 ユーザーがアクセスできる他のユーザーのプライベート、パブリック メッセージ ストアに、ディスク上のファイル ストアまたはその他の受信したメッセージ内に埋め込まれている、一般に含まれている値を設定したメッセージ内に存在する場合は、前回のトランスポート プロバイダーメッセージを配信します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
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

