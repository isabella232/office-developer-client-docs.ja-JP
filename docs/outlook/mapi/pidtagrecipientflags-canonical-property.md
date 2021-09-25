---
title: PidTagRecipientFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRecipientFlags
api_type:
- COM
ms.assetid: 9fbe537f-b5fe-48a2-803c-653c50c82efd
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 24316203e81ae48f8ef320d7a9f16d08d4120c6e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570934"
---
# <a name="pidtagrecipientflags-canonical-property"></a>PidTagRecipientFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信者の状態を表すビット フィールドを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECIPIENT_FLAGS  <br/> |
|識別子:  <br/> |0x5FFD  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |トランスポート受信者  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは必須ではありません。 設定できる個々のフラグを次に示します。
  
|**値**|**説明**|
|:-----|:-----|
|S (recipSendable、0x00000001)  <br/> |受信者は送信 **可能な出席者** です。 このフラグは **、dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) プロパティでのみ使用されます。  <br/> |
|O (recipOrganizer,0x0000002)  <br/> |この **フラグが設定されている RecipientRow** は、会議の開催者を表します。  <br/> |
|ER (recipExceptionalResponse,0x00000010)  <br/> |出席者が、この RecipientRow が存在する例外に対する応答 **を与えたかどうかを** 示します。 このフラグは、開催者の会議オブジェクトの例外埋め込みメッセージ オブジェクトの **RecipientRow** でのみ使用されます。  <br/> |
|ED (recipExceptionalDeleted,0x00000020)  <br/> |**RecipientRow** は存在しますが、対応する受信者が存在しない場合と同様に処理する必要があります。 このフラグは、開催者の会議オブジェクトの例外埋め込みメッセージ オブジェクトの **RecipientRow** でのみ使用されます。  <br/> |
|X (予約済み、0x00000040)  <br/> |設定する必要があります。  <br/> |
|X (予約済み、0x00000080)  <br/> |設定する必要があります。  <br/> |
|G (recipOriginal、0x00000100)  <br/> |受信者が元の出席者を示します。 このフラグは **、dispidApptUnsendableRecips プロパティでのみ使用** されます。  <br/> |
|X (予約済み、0x00000200)  <br/> |予約済み。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
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

