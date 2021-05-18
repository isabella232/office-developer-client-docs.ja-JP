---
title: PidLidTimeZone 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZone
api_type:
- COM
ms.assetid: ffbab371-1a1d-4aa4-ad31-17549a74513c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b62779567a7dbd298fdd313e90b13fb223e4e47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319272"
---
# <a name="pidlidtimezone-canonical-property"></a>PidLidTimeZone 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
定期的な会議のタイム ゾーンに関する情報を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |LID_TIME_ZONE  <br/> |
|プロパティ セット:  <br/> |PSETID_Meeting  <br/> |
|長い ID (LID):  <br/> |0x0000000C  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは **、dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) プロパティが設定されていない場合にのみ読み取り **、LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) プロパティが TRUE で **、LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) プロパティが FALSE の場合にのみ読み取り可能です。 下の WORD は、タイム ゾーン情報を含むテーブルへのインデックスを指定します。 上の WORD では、最も高いビットだけが読み取りされます。 このビットが設定されている場合、参照されるタイム ゾーンは夏時間 (DST) を観測しません。それ以外の場合は [、[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) に詳細な DST 日付が続きます。 
  
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

