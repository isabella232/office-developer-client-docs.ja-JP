---
title: PidLidAppointmentSubType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAppointmentSubType
api_type:
- COM
ms.assetid: e2e00af3-1fb3-4314-936a-f480674d3d83
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8b9b1b4615893418374b98403e7d519d3f632d07
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591893"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a>PidLidAppointmentSubType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
イベントが 1 日の間であるかどうかを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidApptSubType  <br/> |
|プロパティ セット:  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008215  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |予定表  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、ユーザーが指定した通り、イベントがオールデイ イベントかどうかを指定します。 TRUE の値は、イベントが 1 日のイベントであり、その場合は開始時刻と終了時刻が午前 0 時で、期間が 24 時間の倍数で、少なくとも 24 時間である必要があります。 FALSE の値を指定するか、このプロパティがない場合は、イベントがオールデイ イベントではないかどうかを示します。 クライアントまたはサーバーは、イベントが午前 0 時に開始および終了した場合でも、ユーザーが 24 時間のイベントを作成するときに値を TRUE として受け取る必要があります。
  
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

