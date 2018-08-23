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
ms.openlocfilehash: c9c55aa308072db08e6103418be01f91d0d31a82
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566314"
---
# <a name="pidlidtimezonestruct-canonical-property"></a>PidLidTimeZoneStruct 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
定期的な予定または会議出席依頼の開始と終了時に使用するタイム ゾーンを記述する[TZREG](http://msdn.microsoft.com/en-us/library/bb820983%28v=office.12%29.aspx)構造体の保存形式に対応するストリームが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTimeZoneStruct  <br/> |
|プロパティを設定します。  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008233  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |予定表  <br/> |
   
## <a name="remarks"></a>注釈

Microsoft Office Outlook 2003 では、以前のバージョンの Outlook、およびユーザーが Outlook または Exchange Server によって提供される予定表更新ツールを実行していないのでは、コラボレーション データ オブジェクト (CDO) 1.21 をベースとするアプリケーションは、開始時刻と終了時刻を格納します。予定かの相対的な時間として会議出席依頼を定期的な予定と**dispidTimeZoneStruct**で、予定または会議出席依頼を作成する場所のタイム ゾーンを格納します。 ただし、このスキームは、時間の経過と共にタイム ゾーン規則を変更できるように、ユーザーは、ルールが変更され、不適切なタイミングで発生する前にスケジュールするにいくつかの予定および会議の結果を無視します。 ユーザーと管理者が Windows Vista を実行していない、またはされていて、自動更新を有効にしないのは、このような予定と会議出席依頼の時刻を調整するには、Outlook または Exchange Server によって提供されるツールを再配置する予定表を使用してください。 これらの再配置ツールの予定表と予定表を再配置するための Api の詳細については、[夏時間から標準時のプログラムを使用して予定表を再配置の詳細](http://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)を参照してください。
  
ストリームに**TZREG**構造体を保持する場合、 **dispidTimeZoneStruct**、またはを取得するストリームを解析するとき**dispidTimeZoneStruct**のバイナリ プロパティをコミットするのには次のリトル エンディアンの形式を使用します。 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

このプロパティでは、タイム ゾーン情報を指定するのには定期的に設定され、現地時刻と世界協定時刻 (UTC) との間の時間フィールドに変換する方法を指定します。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

