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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b62779567a7dbd298fdd313e90b13fb223e4e47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319272"
---
# <a name="pidlidtimezone-canonical-property"></a>PidLidTimeZone 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
定期的な会議のタイムゾーンに関する情報を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |LID_TIME_ZONE  <br/> |
|プロパティセット:  <br/> |PSETID_Meeting  <br/> |
|ロング ID (LID):  <br/> |0x0000000C  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、 **dispidapptrecur** ([](pidlidappointmentrecur-canonical-property.md)) プロパティが設定されていない場合にのみ読み取られますが、 **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) プロパティが TRUE で、 **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) プロパティは FALSE です。 下位の単語は、タイムゾーン情報を含むテーブルのインデックスを指定します。 上段の単語からは、最上位のビットだけが読み上げられます。 このビットが設定されている場合、参照されるタイムゾーンは夏時間 (dst) を監視しません。それ以外の場合、 [[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)で詳細に指定されている dst の日付が続きます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

