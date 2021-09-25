---
title: PidLidClipEnd 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidClipEnd
api_type:
- COM
ms.assetid: 17c8db96-80dd-4a7a-9a1b-ab1b37ba616c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 115bf8277089fb74c9c969921cf7cf63793c2891
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630419"
---
# <a name="pidlidclipend-canonical-property"></a>PidLidClipEnd 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
単一インスタンスカレンダー オブジェクトの協定世界時 (UTC) でイベントの終了日時を指定します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidClipEnd  <br/> |
|プロパティ セット:  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008236  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |予定表  <br/> |
   
## <a name="remarks"></a>注釈

単一インスタンスの予定表オブジェクトの場合、イベントの終了日時を UTC で指定します。 定期的な系列の場合、このプロパティは、定期的な系列の最後のインスタンスの日付の午前 0 時を UTC で指定します。この場合、値は 8 月 4500 年 8 月 31 日午後 11 時 59 分である必要があります。
  
このプロパティの値は **、dispidApptEndWhole** ([PidLidAppointmentEndWhole) の値に設定する必要があります](pidlidappointmentendwhole-canonical-property.md)。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

