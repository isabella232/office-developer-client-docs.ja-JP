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
ms.openlocfilehash: 7a7134a037aa4845ae22ab18899d27f1e50d6b7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321323"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a>PidTagScheduleInfoAppointmentTombstone 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
辞退された会議を表すデータブロックの一覧が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SCHDINFO_APPT_TOMBSTONE  <br/> |
|識別子:  <br/> |0x686a  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |空き時間情報  <br/> |
   
## <a name="remarks"></a>解説

データブロックは、次のように定義された32ビット値のヘッダーで始まります。
  
|**値**|**説明**|
|:-----|:-----|
|Identifier  <br/> |このフィールドには、0xBEDEAFCD の値を指定する必要があります。  <br/> |
|headersize  <br/> |このフィールドの値は0x00000014 である必要があります。  <br/> |
|バージョン  <br/> |このフィールドの値は3である必要があります。  <br/> |
|レコード数  <br/> |フォローされているレコードの数。  <br/> |
|レコードサイズ  <br/> |このフィールドの値は0x00000014 である必要があります。  <br/> |
   
ヘッダーの後には、次のように定義された32ビット値の**レコード数**エントリが続きます。 
  
|**値**|**説明**|
|:-----|:-----|
|StartTime  <br/> |会議オブジェクトの開始時刻を、1601年1月1日午前0時からの経過時間 (分) で示します。  <br/> |
|EndTime  <br/> |会議オブジェクトの終了時刻を、1601年1月1日午前0時からの経過時間 (分) で示します。  <br/> |
|GlobalObjectIdSize  <br/> |globalobjectid フィールドのサイズ (バイト単位)。  <br/> |
|globalobjectid  <br/> |このレコードが表す会議の**LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) プロパティの値。  <br/> |
|UserName  <br/> |最初の2バイトは、その後に続く PT_STRING8 文字列の長さです。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

