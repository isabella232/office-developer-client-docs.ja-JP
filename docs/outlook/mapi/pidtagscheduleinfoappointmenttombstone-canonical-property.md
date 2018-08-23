---
title: PidTagScheduleInfoAppointmentTombstone 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAppointmentTombstone
api_type:
- COM
ms.assetid: 6b82e2ee-992f-4cbe-bdcb-e7465e556640
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 37a6d101f6ee9c04236253e143aff3a51a9208d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803460"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a>PidTagScheduleInfoAppointmentTombstone 標準プロパティ

  
  
**適用対象**: Outlook 
  
辞退された会議を表すデータ ブロックのリストが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SCHDINFO_APPT_TOMBSTONE  <br/> |
|識別子:  <br/> |0x686A  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |空き/予約済み  <br/> |
   
## <a name="remarks"></a>注釈

データ ブロックは、32 ビットの値として定義されているヘッダーで始まります。
  
|**値**|**説明**|
|:-----|:-----|
|Identifier  <br/> |このフィールドには、0xBEDEAFCD の値を指定する必要があります。  <br/> |
|HeaderSize  <br/> |0x00000014 の値がこのフィールドに必要です。  <br/> |
|バージョン  <br/> |このフィールドには、値 3 が必要です。  <br/> |
|RecordsCount  <br/> |以下のレコードの数。  <br/> |
|RecordsSize  <br/> |0x00000014 の値がこのフィールドに必要です。  <br/> |
   
ヘッダーには、32 ビットの値として定義されているの**RecordsCount**エントリが続きます。 
  
|**値**|**説明**|
|:-----|:-----|
|StartTime  <br/> |1601 年 1 月 1 日午前 0: 00 UTC 以降の分で、会議オブジェクトの開始時刻。  <br/> |
|EndTime  <br/> |1601 年 1 月 1 日午前 0: 00 UTC からの分単位の会議オブジェクトの終了時間です。  <br/> |
|GlobalObjectIdSize  <br/> |GlobalObjectId フィールドのバイト単位のサイズです。  <br/> |
|GlobalObjectId  <br/> |会議のレコードの**LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) プロパティの値を表します。  <br/> |
|UserName  <br/> |最初の 2 バイトは、後に続く PT_STRING8 文字列の長さです。  <br/> |
   
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
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

