---
title: PidLidAppointmentTimeZoneDefinitionRecur 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionRecur
api_type:
- COM
ms.assetid: 52fd57a0-9e34-4452-9ecd-2acb454446c9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e5e9b06178a1517fc1c8652b0d667faf1afc77cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345354"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a>PidLidAppointmentTimeZoneDefinitionRecur 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx)構造の永続形式にマップするストリームを格納します。このストリームには、定期的な予定または会議出席依頼の作成時に使用されるタイムゾーンの説明を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidApptTZDefRecur  <br/> |
|プロパティセット:  <br/> |PSETID_Appointment  <br/> |
|ロング ID (LID):  <br/> |0x00008260  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |カレンダー  <br/> |
   
## <a name="remarks"></a>解説

microsoft Office outlook 2007 以降のバージョンの microsoft outlook と、outlook または Exchange Server 予定表更新ツールを実行したコラボレーションデータオブジェクト (CDO) 1.2.1 に基づくソリューションは、 **dispidApptTZDefRecur**と**を使用します。dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) プロパティを使用して、タイムゾーンのルールが変更された場合に、定期的な会議を調整する必要があるかどうかを判断します。 以前のクライアントでは、 **dispidTimeZoneStruct**プロパティを引き続き操作できるため、これらのプロパティを同期する必要があります。 2つのプロパティが同期されているかどうかを検出するには、 **dispidTimeZoneStruct**に一致するルールの**wflags**メンバに TZRULE_FLAG_RECUR_CURRENT_TZREG フラグを設定する必要があります。 このフラグが設定されていない場合、または設定されていて、 **dispidTimeZoneStruct**プロパティのルールがマークされたルールと一致しない場合は、 **dispidApptTZDefRecur**プロパティを破棄して、代わりに**dispidTimeZoneStruct**を使用する必要があります。 
  
**dispidApptTZDefRecur**プロパティと**dispidTimeZoneStruct**プロパティの両方を新しい定期的な会議に書き込む場合、または**dispidTimeZoneStruct**プロパティを使用する任意の選択肢を作成する場合は、タイムゾーンの現在の定義 (Windows レジストリに従う) を使用する必要があります。 
  
パーサーは、 **dispidApptTZDefRecur**から取得されたストリームを読み取るとき、または**dispidApptTZDefRecur**などのバイナリプロパティへのコミットメントを得るために**TZDEFINITION**に保持されている場合は、注意を払う必要があります。 詳細については、「データを[バイナリプロパティにコミットするためのストリームへの永続化 TZDEFINITION](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)」を参照してください。
  
 **dispidApptTZDefRecur**は、定期的な会議の日付と時刻を協定世界時 (UTC) との間で変換する方法を示すタイムゾーン情報を指定します。 このプロパティが設定されていて、 **dispidTimeZoneStruct**によって表されるデータと矛盾するデータがある場合、クライアントは**dispidApptTZDefRecur**ではなく**dispidTimeZoneStruct**を使用する必要があります。 **dispidApptTZDefRecur**が設定されていない場合は、 **PidLidTimeZoneStruct**プロパティが代わりに使用されます。 この BLOB のフィールドは、リトルエンディアンバイト順でエンコードされます。 
  
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

