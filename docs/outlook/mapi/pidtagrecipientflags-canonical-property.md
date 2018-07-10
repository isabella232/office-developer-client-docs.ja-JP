---
title: PidTagRecipientFlags の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a93e5a44768cd99512189f800bf98ab6e30b575d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803271"
---
# <a name="pidtagrecipientflags-canonical-property"></a>PidTagRecipientFlags の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
受信者の状態を示すビット フィールドを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_RECIPIENT_FLAGS  <br/> |
|識別子:  <br/> |0x5FFD  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |トランスポートにおける受取人  <br/> |
   
## <a name="remarks"></a>備考

このプロパティが必要ではありません。 設定可能な個々 のフラグを次に示します。
  
|**値**|**説明**|
|:-----|:-----|
|S (recipSendable、0x00000001)  <br/> |受信者は、 **Sendable**の参加者です。 このフラグは、 **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) のプロパティでのみ使用されます。  <br/> |
|O (recipOrganizer、0x0000002)  <br/> |このフラグが設定される**RecipientRow**は、会議の開催者を表します。  <br/> |
|ER (recipExceptionalResponse、0x00000010)  <br/> |出席者がこの**RecipientRow**が格納されている例外の応答を与えたことを示します。 このフラグは、 **RecipientRow**の開催者の会議オブジェクトの例外メッセージを埋め込みオブジェクトでのみ使用されます。  <br/> |
|ED (recipExceptionalDeleted、0x00000020)  <br/> |**RecipientRow**が存在しますが、その扱うこと、対応する受信者がいない場合とを示します。 このフラグは、 **RecipientRow**の開催者の会議オブジェクトの例外メッセージを埋め込みオブジェクトでのみ使用されます。  <br/> |
|(予約済み、0x00000040) x  <br/> |設定する必要があります。  <br/> |
|(予約済み、0x00000080) x  <br/> |設定する必要があります。  <br/> |
|G (recipOriginal、0x00000100)  <br/> |受信者が元の出席者であることを示します。 このフラグは、 **dispidApptUnsendableRecips**プロパティでのみ使用されます。  <br/> |
|(予約済み、0x00000200) x  <br/> |予約済み。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
