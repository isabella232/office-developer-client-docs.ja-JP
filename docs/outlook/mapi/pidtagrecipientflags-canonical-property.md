---
title: PidTagRecipientFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientFlags
api_type:
- COM
ms.assetid: 9fbe537f-b5fe-48a2-803c-653c50c82efd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7b791d75c2a76ea1a504c0d8862dd20f5365b475
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356701"
---
# <a name="pidtagrecipientflags-canonical-property"></a>PidTagRecipientFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信者の状態を示すビットフィールドを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECIPIENT_FLAGS  <br/> |
|識別子:  <br/> |0x5ffd  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |トランスポート受信者  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは必須ではありません。 設定できる個別のフラグを次に示します。
  
|**値**|**説明**|
|:-----|:-----|
|S (recipSendable、0x00000001)  <br/> |受信者が**送信可能**の出席者である。 このフラグは、 **dispidapptunsendablerPidLidAppointmentUnsendableRecipients** ([](pidlidappointmentunsendablerecipients-canonical-property.md)) プロパティでのみ使用されます。  <br/> |
|O (recipOrganizer、0x0000002)  <br/> |このフラグが設定されている**受信者行**は、会議開催者を表します。  <br/> |
|ER (recipExceptionalResponse、0x00000010)  <br/> |出席者が、この**受信者行**が存在する例外の応答を受け取ったことを示します。 このフラグは、開催者の会議オブジェクトの埋め込みメッセージオブジェクトの [**受信者] 行**でのみ使用されます。  <br/> |
|ED (recipExceptionalDeleted, 0x00000020)  <br/> |[**受信者] 行**が存在していても、対応する受信者が指定されていない場合と同様に扱われることを示します。 このフラグは、開催者の会議オブジェクトの埋め込みメッセージオブジェクトの [**受信者] 行**でのみ使用されます。  <br/> |
|X (予約済み、0x00000040)  <br/> |設定することはできません。  <br/> |
|X (予約済み、0x00000080)  <br/> |設定することはできません。  <br/> |
|G (recipOriginal, 0x00000100)  <br/> |受信者が元の出席者であることを示します。 このフラグは、 **dispidapptunsendablerな ps**プロパティでのみ使用されます。  <br/> |
|X (予約済み、0x00000200)  <br/> |予約済み。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
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

