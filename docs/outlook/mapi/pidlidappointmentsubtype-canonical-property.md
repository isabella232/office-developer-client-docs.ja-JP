---
title: PidLidAppointmentSubType の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentSubType
api_type:
- COM
ms.assetid: e2e00af3-1fb3-4314-936a-f480674d3d83
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: cb9f4e0f58ea27d36ba911ed60527a2e53f23727
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801804"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a>PidLidAppointmentSubType の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
イベントが 1 日であるかどうかを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidApptSubType  <br/> |
|プロパティを設定します。  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008215  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |カレンダー  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、イベントは、終日イベントでは、ユーザーが指定されているかどうかを指定します。 TRUE の値は、イベントが終日イベントでは、場合に、開始時刻と終了時刻する必要があることで、午前 0 時 24 時間の倍数の期間とは、少なくとも 24 時間を示します。 値が FALSE の場合、またはこのプロパティがない場合は、イベントが終日イベントではないことを示します。 クライアントまたはサーバーではイベントが開始され、午前 0 時に終了した場合でも、ユーザーが 24 時間であるイベントを作成する場合、値は TRUE としてを推測こと必要がありますいません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
