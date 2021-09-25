---
title: PidTagMessageToMe 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageToMe
api_type:
- HeaderDef
ms.assetid: aeb0fa71-f471-46c5-ad9c-f8afb3fed533
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 70de6eea896ee09ae5846589a88d58f0ac261f92
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629761"
---
# <a name="pidtagmessagetome-canonical-property"></a>PidTagMessageToMe 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このメッセージング ユーザーが、このメッセージのプライマリ (宛先) 受信者として特別に名前が付け、配布リストの一部ではない場合は TRUE を含む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MESSAGE_TO_ME  <br/> |
|識別子:  <br/> |0x0057  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、リスト内のすべてのエントリを調べることなく、ユーザー名がプライマリ受信者リストに明示的に表示されるかどうかを判断する便利な方法を提供します。 
  
このプロパティは、受信時の受信メッセージの自動処理も支援します。 トランスポート プロバイダーのオプションでは、このプロパティに FALSE が含まれているか、メッセージング ユーザーが受信者テーブルに直接表示されていない場合は含まれません。 
  
配布リストの拡張やブラインド カーボン コピーの指定によって生じるメッセージ配信では、このプロパティは設定されません。 受信者の名前は明示的に指定する必要があります。 
  
非送信メッセージは、通常、PR_MESSAGE_CC_ME **(** [PidTagMessageCcMe)](pidtagmessageccme-canonical-property.md) **、PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe)](pidtagmessagerecipientme-canonical-property.md)、またはこのプロパティを設定しません。 ユーザーがメッセージに存在する場合、ユーザーはパブリック メッセージ ストア、他のユーザーのプライベート ストア、ディスク上のファイル、または他の受信メッセージ内に埋め込まれている場合、通常、トランスポート プロバイダーがメッセージを最後に配信した時刻に設定された値を含みます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
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

