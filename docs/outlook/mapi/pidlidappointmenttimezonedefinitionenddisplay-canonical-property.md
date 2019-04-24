---
title: PidLidAppointmentTimeZoneDefinitionEndDisplay 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionEndDisplay
api_type:
- COM
ms.assetid: 7b6193cb-612b-408e-b9bc-285df313e2cc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 24ccd25a1d799f3146bd230e5156be0051104f47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345382"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a>PidLidAppointmentTimeZoneDefinitionEndDisplay 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx)構造の永続形式にマップするストリームを格納します。これは、単一インスタンスの予定または会議出席依頼の終了時刻が選択されたときに使用されるタイムゾーンの説明を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidApptTZDefEndDisplay  <br/> |
|プロパティセット:  <br/> |PSETID_Appointment  <br/> |
|ロング ID (LID):  <br/> |0x0000825f  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |カレンダー  <br/> |
   
## <a name="remarks"></a>解説

microsoft Office Outlook 2003 またはそれ以前のバージョンで、コラボレーションデータオブジェクト (CDO) 1.2.1 に基づいていて、Outlook または Microsoft Exchange Server 用の予定表更新ツールを実行していない場合は、単一インスタンスの開始時刻と終了時刻を格納します。協定世界時 (UTC) の予定および会議出席依頼。 これらのクライアントには、予定または会議出席依頼が作成されたタイムゾーンの情報は格納されません。
  
microsoft Office outlook 2007 以降のバージョンの microsoft outlook と、outlook または Exchange Server 予定表更新ツールを実行した CDO 1.2.1 に基づくソリューションは、 **dispidApptTZDefEndDisplay**を使用して、終了時刻のタイムゾーンを格納します。 **dispidApptTZDefEndDisplay**は、スケジュールされた元のタイムゾーンで予定または会議を表示し、タイムゾーンのルールが変更された場合に終了時刻を調整する必要があるかどうかを決定します。 このプロパティが指定されていない場合、 **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) プロパティによって指定されたタイムゾーンが使用されます。 **dispidApptTZDefStartDisplay**が見つからないか無効である場合は、現在のローカルタイムゾーンが想定されます。 **dispidApptTZDefEndDisplay**は表示のみを目的として使用され、定期的な展開では使用されません。 
  
パーサーは、 **dispidApptTZDefEndDisplay**から取得されたストリームを読み取るとき、または**dispidApptTZDefEndDisplay**などのバイナリプロパティへのコミットメントを得るために**TZDEFINITION に**に永続化するときに、注意を払う必要があります。 詳細については、「データを[バイナリプロパティにコミットするためのストリームへの永続化 TZDEFINITION](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)」を参照してください。
  
 **dispidApptTZDefEndDisplay**は、 **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) プロパティのタイムゾーン情報を指定します。 **dispidApptTZDefEndDisplay**の形式、制約、および計算は、 **dispidApptTZDefStartDisplay**プロパティで指定したものと同じです。 
  
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

