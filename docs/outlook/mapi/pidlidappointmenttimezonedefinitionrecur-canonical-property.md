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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389303"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a>PidLidAppointmentTimeZoneDefinitionRecur 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
定期的な予定または会議出席依頼の作成時に使用されるタイム ゾーンの説明を格納する[TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx)構造体の保存形式に対応するストリームが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidApptTZDefRecur  <br/> |
|プロパティを設定します。  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008260  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |予定表  <br/> |
   
## <a name="remarks"></a>備考

Outlook または Exchange Server の予定表を実行している Microsoft Outlook を Microsoft Office Outlook 2007 では、ソリューションでは、コラボレーション データ オブジェクト (CDO) 1.2.1 以降のバージョンは、ツールの使用方法**dispidApptTZDefRecur**と**を更新します。dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) のプロパティをタイム ゾーンの規則を変更する場合に、定期的な会議を調整する必要があるかどうかを確認します。 古いクライアントが、 **dispidTimeZoneStruct**プロパティを操作するため、これらのプロパティを同期する必要があります。 2 つのプロパティーを同期するかどうかを検出するには、 **dispidTimeZoneStruct**に一致するルールの**wFlags**メンバーに、TZRULE_FLAG_RECUR_CURRENT_TZREG フラグを設定する必要があります。 このフラグは設定されていない、または設定されている、 **dispidTimeZoneStruct**プロパティの規則は、マークされたルールと一致しない場合、 **dispidApptTZDefRecur**プロパティを破棄する必要があり、 **dispidTimeZoneStruct**を代わりに使用する必要があります。 
  
新しい定期的な会議、または、 **dispidTimeZoneStruct**プロパティ、タイム ゾーン (の現在の定義を使用して任意の選択を行うと、 **dispidApptTZDefRecur**と**dispidTimeZoneStruct**の両方のプロパティを記述する場合Windows レジストリ) に従って使用する必要があります。 
  
パーサーは、 **dispidApptTZDefRecur**から取得するストリームを読み取るとき、または**dispidApptTZDefRecur**などのバイナリのプロパティへの取り組みのためのストリームに**TZDEFINITION**が引き続き発生する場合注意が必要である必要があります。 詳細については、[バイナリのプロパティをコミットするためのストリームに永続化する TZDEFINITION](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)を参照してください。
  
 **dispidApptTZDefRecur**を世界協定時刻 (UTC) から、会議の日付と時刻、定期的に変換する方法を説明するタイム ゾーン情報を指定します。 このプロパティが**dispidTimeZoneStruct**で表されるデータと一致しないデータがある場合は、クライアントは、 **dispidApptTZDefRecur**の代わりに**dispidTimeZoneStruct**を使用する必要があります。 **DispidApptTZDefRecur**が設定されていない場合、 **PidLidTimeZoneStruct**プロパティが使用されます。 この BLOB 内のフィールドは、リトル エンディアン バイト順でエンコードされます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

