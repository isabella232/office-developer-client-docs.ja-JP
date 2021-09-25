---
title: PidLidTimeZoneStruct 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTimeZoneStruct
api_type:
- COM
ms.assetid: 2acf0036-2f3e-4f90-8614-7aa667860f74
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2b7d2e0b7487743edcab993a00607144c36327ee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579356"
---
# <a name="pidlidtimezonestruct-canonical-property"></a>PidLidTimeZoneStruct 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
定期的な予定または会議出席依頼の開始時刻と終了時刻に使用するタイム ゾーンを示す [、TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) 構造の永続化された形式にマップするストリームが含まれます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTimeZoneStruct  <br/> |
|プロパティ セット:  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008233  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |予定表  <br/> |
   
## <a name="remarks"></a>注釈

Microsoft Office Outlook 2003、以前のバージョンの Outlook、およびコラボレーション データ オブジェクト (CDO) 1.21 に基づくアプリケーションで、ユーザーが Outlook または Exchange Server が提供する予定表更新ツールを実行していない場合は、定期的な予定または会議出席依頼の開始時刻と終了時刻を相対時間として保存し、st予定または会議出席依頼が **dispidTimeZoneStruct** で作成されるタイム ゾーンを ore します。 ただし、このスキームでは、時間がたつ間にタイム ゾーン ルールが変更され、ルールが変更される前にスケジュールされた予定や会議が発生する可能性があります。 Windows Vista を実行していない、または自動更新を有効にしていないユーザーと管理者は、Outlook または Exchange Server によって提供される予定表の再調整ツールを使用して、そのような予定や会議出席依頼の時間を調整する必要があります。 予定表をリベースするこれらの予定表の再調整ツールと API の詳細については、「夏時間に合わせてプログラムで予定表を再調整する方法について[」を参照してください](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)。
  
**dispidTimeZoneStruct** から取得したストリームを解析する場合、または **TZREG** 構造体をストリームに永続化して **dispidTimeZoneStruct** バイナリ プロパティにコミットする場合は、次のリトルエンディアン形式を使用します。 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

このプロパティは、タイム ゾーン情報を指定するために定期的な系列に設定され、時刻フィールドを現地時間と協定世界時 (UTC) の間で変換する方法を指定します。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
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

