---
title: PidLidAppointmentRecur 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentRecur
api_type:
- COM
ms.assetid: 56d6240f-d07b-48d1-aef0-bf57078ea6c3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: de50616664048af6b931a09df7c65461e9ee3399
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331781"
---
# <a name="pidlidappointmentrecur-canonical-property"></a>PidLidAppointmentRecur 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)で指定されている繰り返しパターンと範囲のいずれかを使用して、定期的な系列が発生する日時を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidApptRecur  <br/> |
|プロパティ セット:  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008216  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |カレンダー  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは [、[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)で説明されている繰り返しパターンと範囲のいずれかを使用して、定期的な系列が発生する日時を指定します。 このプロパティの値には、変更された例外と削除された例外の両方に関する情報も含まれる。日付、件名、場所、および例外の他のいくつかのプロパティなどの情報。 定期的な予定表アイテムのこのプロパティのバイナリ データは **、AppointmentRecurrencePattern 構造体として格納** されます。 このプロパティは、単一インスタンスの予定表アイテムに存在していなければなりません。 
  
繰り返しにはいくつかの制限があります。
  
- 複数のインスタンスが同じ日に開始される必要があります。
    
- オカレンスは重なってはなりません。 具体的には、定期的な系列内のインスタンスの開始日を変更する例外は、前のインスタンスの終了および定期的な系列の次のインスタンスの開始後の日付に発生する必要があります。 定期的なシリーズの前または次のインスタンスが例外である場合も同様です。
    
定期的な系列のスケジュールは、定期的なパターンと範囲によって決まります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> メールなどのオブジェクトアラームのプロパティと対話モデルを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

