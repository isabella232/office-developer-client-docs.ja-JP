---
title: PidLidTimeZoneStruct 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZoneStruct
api_type:
- COM
ms.assetid: 2acf0036-2f3e-4f90-8614-7aa667860f74
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b9c2a1bbf519379c1735c489c2dcd3fcfb395a60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346376"
---
# <a name="pidlidtimezonestruct-canonical-property"></a>PidLidTimeZoneStruct 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx)構造の永続形式にマップするストリームを格納します。これは、定期的な予定または会議出席依頼の開始時刻と終了時刻に使用されるタイムゾーンを表します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTimeZoneStruct  <br/> |
|プロパティセット:  <br/> |PSETID_Appointment  <br/> |
|ロング ID (LID):  <br/> |0x00008233  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |カレンダー  <br/> |
   
## <a name="remarks"></a>解説

Microsoft Office outlook 2003、以前のバージョンの outlook、およびユーザーが outlook または Exchange Server ストアが提供する予定表更新ツールを実行していないグループ作業データオブジェクト (CDO) 1.21 に基づくアプリケーション相対時間としての定期的な予定または会議出席依頼。 **dispidTimeZoneStruct**で予定または会議出席依頼が作成されたタイムゾーンを保存します。 ただし、このスキームでは時間が経過すると、タイムゾーンの規則が変化し、ルールが変更される前にユーザーがスケジュールを設定して、誤った時間に発生する予定と会議を作成することができます。 Windows Vista を実行していない、または自動更新が有効になっていないユーザーと管理者は、Outlook または Exchange Server によって提供される予定表の再配置ツールを使用して、そのような予定や会議出席依頼の時刻を調整する必要があります。 カレンダーを再配置するための、これらの予定表の再配置ツールと api の詳細については、「[夏時間のプログラムを使用して予定表](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)を再配置する」をご覧ください。
  
**dispidTimeZoneStruct**から取得したストリームを解析するとき、または**TZREG**構造体を**dispidTimeZoneStruct** binary プロパティにコミットするストリームに永続化するときは、次のリトルエンディアン形式を使用します。 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

このプロパティは、タイムゾーン情報を指定するために定期的なアイテムに対して設定され、時刻フィールドを現地時刻と協定世界時 (UTC) の間で変換する方法を指定します。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
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

