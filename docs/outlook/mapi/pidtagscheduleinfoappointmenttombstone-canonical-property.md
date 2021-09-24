---
title: PidTagScheduleInfoAppointmentTombstone 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagScheduleInfoAppointmentTombstone
api_type:
- COM
ms.assetid: 6b82e2ee-992f-4cbe-bdcb-e7465e556640
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1e89049186dfe32e6e76cd52324ef9aad37d8a82
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550464"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a>PidTagScheduleInfoAppointmentTombstone 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
拒否された会議を表すデータ ブロックの一覧が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SCHDINFO_APPT_TOMBSTONE  <br/> |
|識別子:  <br/> |0x686A  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |空き時間情報  <br/> |
   
## <a name="remarks"></a>注釈

データ ブロックは、次のように定義された 32 ビット値のヘッダーで始まります。
  
|**値**|**説明**|
|:-----|:-----|
|識別子  <br/> |このフィールドは、次の値0xBEDEAFCD。  <br/> |
|HeaderSize  <br/> |このフィールドには、値が0x00000014。  <br/> |
|バージョン  <br/> |このフィールドの値は 3 である必要があります。  <br/> |
|RecordsCount  <br/> |続くレコードの数。  <br/> |
|RecordsSize  <br/> |このフィールドには、値が0x00000014。  <br/> |
   
ヘッダーの後に、次のように定義された 32 ビット値の **RecordsCount** エントリが続きます。 
  
|**値**|**説明**|
|:-----|:-----|
|StartTime  <br/> |会議オブジェクトの開始時刻 (1601 年 1 月 1 日午前 0 時から分) (UTC)。  <br/> |
|EndTime  <br/> |1601 年 1 月 1 日午前 0 時以降の会議オブジェクトの終了時刻 (分)。  <br/> |
|GlobalObjectIdSize  <br/> |GlobalObjectId フィールドのサイズ (バイト単位)。  <br/> |
|GlobalObjectId  <br/> |このレコードが表 **す会議LID_GLOBAL_OBJID** [(PidLidGlobalObjectId)](pidlidglobalobjectid-canonical-property.md)プロパティの値を指定します。  <br/> |
|UserName  <br/> |最初の 2 バイトは、次の文字列PT_STRING8長さです。  <br/> |
   
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

