---
title: PidLidAppointmentTimeZoneDefinitionRecur 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAppointmentTimeZoneDefinitionRecur
api_type:
- COM
ms.assetid: 52fd57a0-9e34-4452-9ecd-2acb454446c9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 83e72d3862ef38d93dace38b91e7a8a70ecb538c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583934"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a>PidLidAppointmentTimeZoneDefinitionRecur 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
定期的な予定または会議出席依頼の作成時に使用されるタイム ゾーンの説明を格納する [、TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) 構造体の永続化された形式にマップするストリームを格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidApptTZDefRecur  <br/> |
|プロパティ セット:  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008260  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |予定表  <br/> |
   
## <a name="remarks"></a>注釈

Microsoft Office Outlook 2007 以降の Microsoft Outlook のバージョン、および Outlook または Exchange Server カレンダー更新ツールを実行したコラボレーション データ オブジェクト (CDO) 1.2.1 に基づくソリューションでは **、dispidApptTZDefRecur** プロパティと **dispidTimeZoneStruct** [(PidLidTimeZoneStruct)](pidlidtimezonestruct-canonical-property.md)プロパティを使用して、次の操作を実行します。タイム ゾーンのルールが変更された場合に定期的な会議を調整するかどうかを決定します。 古いクライアントが **dispidTimeZoneStruct** プロパティを操作する場合もありますので、これらのプロパティを同期する必要があります。 2 つのプロパティが同期されているかどうかを検出するには **、dispidTimeZoneStruct** に一致するルールの **wFlags** メンバーに、TZRULE_FLAG_RECUR_CURRENT_TZREGフラグが設定されている必要があります。 このフラグが設定されていない場合、または設定され **、dispidTimeZoneStruct** プロパティのルールがマークされたルールと一致しない場合は **、dispidApptTZDefRecur** プロパティを破棄し、代わりに **dispidTimeZoneStruct** を使用する必要があります。 
  
**dispidApptTZDefRecur** プロパティと **dispidTimeZoneStruct** プロパティの両方を新しい定期的な会議に書き込む場合、または **dispidTimeZoneStruct** プロパティを使用する任意の選択を行う場合は、(Windows レジストリに従って) タイム ゾーンの現在の定義を使用する必要があります。 
  
パーサーは **、dispidApptTZDefRecur** から取得されたストリームを読み取る場合、または **TZDEFINITION** をストリームに保持して **、dispidApptTZDefRecur** などのバイナリ プロパティへのコミットメントを行う場合には注意する必要があります。 詳細については [、「TZDEFINITION をストリーム](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)に永続化してバイナリ プロパティにコミットする方法について」を参照してください。
  
 **dispidApptTZDefRecur** は、定期的なシリーズの会議の日時を協定世界時 (UTC) との間で変換する方法を説明するタイム ゾーン情報を指定します。 このプロパティが設定されているが **、dispidTimeZoneStruct** で表されるデータと矛盾するデータがある場合、クライアントは **dispidApptTZDefRecur** ではなく **dispidTimeZoneStruct** を使用する必要があります。 **dispidApptTZDefRecur** が設定されていない場合は **、PidLidTimeZoneStruct** プロパティが代わりに使用されます。 この BLOB のフィールドは、リトル エンドのバイト順でエンコードされます。 
  
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

