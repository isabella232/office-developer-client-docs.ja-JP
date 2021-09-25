---
title: PidLidAppointmentTimeZoneDefinitionEndDisplay 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAppointmentTimeZoneDefinitionEndDisplay
api_type:
- COM
ms.assetid: 7b6193cb-612b-408e-b9bc-285df313e2cc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 442de37a31b53384a9ce4cc5ef24b8f33a6c6d6c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583927"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a>PidLidAppointmentTimeZoneDefinitionEndDisplay 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
単一インスタンスの予定または会議出席依頼の終了時刻が選択されている場合に使用されるタイム ゾーンの説明を格納する [、TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) 構造体の永続化された形式にマップするストリームを格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidApptTZDefEndDisplay  <br/> |
|プロパティ セット:  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x0000825F  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |予定表  <br/> |
   
## <a name="remarks"></a>注釈

Microsoft Office Outlook 2003 以前、およびコラボレーション データ オブジェクト (CDO) 1.2.1 に基づいており、Outlook または Microsoft Exchange Server の予定表更新ツールを実行していないソリューションでは、1 インスタンスの予定と会議出席依頼の開始時刻と終了時刻を協定世界時 (UTC) に保存します。 これらのクライアントには、予定または会議出席依頼が作成されるタイム ゾーンの情報は保存されません。
  
Microsoft Office Outlook 2007 以降の Microsoft Outlook のバージョンと、Outlook または Exchange Server カレンダー更新ツールを実行した CDO 1.2.1 に基づくソリューションでは **、dispidApptTZDefEndDisplay** を使用して終了時刻のタイム ゾーンを格納します。 **dispidApptTZDefEndDisplay** は、スケジュールされた元のタイム ゾーンの予定または会議を表示し、タイム ゾーンのルールが変更された場合に終了時刻を調整するかどうかを決定します。 このプロパティが見つからない場合は **、dispidApptTZDefStartDisplay** [(PidLidAppointmentTimeZoneDefinitionStartDisplay)](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)プロパティで指定されたタイム ゾーンが使用されます。 **dispidApptTZDefStartDisplay** が見つからないか無効な場合、現在のローカル タイム ゾーンが想定されます。 **dispidApptTZDefEndDisplay** は表示目的でのみ使用され、定期的な展開では使用されません。 
  
パーサーは **、dispidApptTZDefEndDisplay** から取得したストリームを読み取る場合、または **dispidApptTZDefEndDisplay** などのバイナリ プロパティへのコミットメントのために **TZDEFINITION** をストリームに保持するときに注意する必要があります。 詳細については [、「TZDEFINITION をストリーム](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)に永続化してバイナリ プロパティにコミットする方法について」を参照してください。
  
 **dispidApptTZDefEndDisplay は****、dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) プロパティのタイム ゾーン情報を指定します。 **dispidApptTZDefEndDisplay** の形式、制約、および計算は **、dispidApptTZDefStartDisplay** プロパティで指定した形式と同じです。 
  
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

