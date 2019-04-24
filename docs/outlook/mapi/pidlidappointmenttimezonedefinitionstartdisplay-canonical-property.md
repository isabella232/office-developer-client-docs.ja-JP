---
title: PidLidAppointmentTimeZoneDefinitionStartDisplay 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionStartDispl
api_type:
- COM
ms.assetid: 08239670-3211-420c-99d7-0056ed967cb8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 504dc4b1cecb9798590e4a15968acc3aa98fe4a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345018"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a>PidLidAppointmentTimeZoneDefinitionStartDisplay 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx)構造の永続形式にマップするストリームを格納します。これは、単一インスタンスの予定または会議出席依頼の開始時刻が選択されたときに使用されるタイムゾーンの説明を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidApptTZDefStartDisplay  <br/> |
|プロパティセット:  <br/> |PSETID_Appointment  <br/> |
|ロング ID (LID):  <br/> |0x0000825e  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |カレンダー  <br/> |
   
## <a name="remarks"></a>解説

microsoft Office Outlook 2003 またはそれ以前のバージョンで、コラボレーションデータオブジェクト (CDO) 1.2.1 に基づいていて、Outlook または Microsoft Exchange Server 用の予定表更新ツールを実行していない場合は、単一インスタンスの開始時刻と終了時刻を格納します。協定世界時 (UTC) の予定および会議出席依頼。 これらのクライアントには、予定または会議出席依頼が作成されたタイムゾーンの情報は格納されません。
  
Microsoft Office outlook 2007 以降のバージョンの outlook と、outlook または Exchange Server 予定表更新ツールを実行した CDO 1.2.1 に基づくソリューションこのプロパティを使用して、開始時刻のタイムゾーンを保存します。 **dispidApptTZDefStartDisplay**プロパティは、スケジュールされた元のタイムゾーンで予定または会議を表示します。 タイムゾーンのルールが変更された場合に、開始時刻を調整するかどうかを決定します。 このプロパティが存在しない場合は、現在のローカルタイムゾーンが想定されます。 このプロパティは表示のみを目的として使用され、定期的な展開では使用されません。 
  
パーサーは、このプロパティから取得されたストリームを読み取るとき、または**dispidApptTZDefStartDisplay**などのバイナリプロパティへのコミットメントを**TZDEFINITION**に保持するときに、注意を払う必要があります。 詳細については、「データを[バイナリプロパティにコミットするためのストリームへの永続化 TZDEFINITION](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)」を参照してください。
  
このプロパティは、 **dispidapptstartwhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) プロパティのタイムゾーン情報を指定します。 **dispidApptTZDefStartDisplay**の値は、表示を目的として、開始日と時刻を UTC からローカルタイムゾーンに変換するために使用されます。 このプロパティで指定された**TZRULE**ごとに、TZRULE_FLAG_RECUR_CURRENT_TZREG フラグを設定してはなりません。 たとえば、 **TZRULE**が有効なルールである場合、フィールドの値**TZRULE**は "0x0002" である必要があります。それ以外の場合は、"0x0000" である必要があります。 
  
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

