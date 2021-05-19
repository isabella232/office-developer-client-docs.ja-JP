---
title: PidLidAppointmentStartWhole 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentStartWhole
api_type:
- COM
ms.assetid: e5e8ed98-57af-40d0-85c4-9d9832626e6b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6f9fb9c3f02e66fd01e89742edcfba7391c36e3e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345375"
---
# <a name="pidlidappointmentstartwhole-canonical-property"></a>PidLidAppointmentStartWhole 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
予定が開始される日時を表します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidApptStartWhole  <br/> |
|プロパティ セット:  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x0000820D  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |カレンダー  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、イベントの開始日時を指定します。 このプロパティは協定世界時 (UTC) で **、dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) プロパティの値より小さい必要があります。 定期的な系列の場合、このプロパティは、定期的なパターンに従って最初のインスタンスの開始日時です。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様Exchange Server提供します。
    
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

