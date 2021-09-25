---
title: PidLidAppointmentEndWhole 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAppointmentEndWhole
api_type:
- COM
ms.assetid: f6fd33d6-04fb-4801-a004-fb80a14ca79d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6f0817a02f3a6661032e5e0c67be151d322a036c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625106"
---
# <a name="pidlidappointmentendwhole-canonical-property"></a>PidLidAppointmentEndWhole 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
予定が終了する日時を表します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidApptEndWhole  <br/> |
|プロパティ セット:  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x0000820E  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |予定表  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、オブジェクト モデル内の予定の **dispidApptEndWhole** プロパティMicrosoft Office Outlook対応します。 
  
これは、イベントの終了日時を指定します。協定世界時 (UTC) で **、dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) プロパティの値より大きくする必要があります。 定期的な系列の場合 **、dispidApptEndWhole** プロパティは、定期的なパターンに従って最初のインスタンスの終了日時です。 
  
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

