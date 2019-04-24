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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: de50616664048af6b931a09df7c65461e9ee3399
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331781"
---
# <a name="pidlidappointmentrecur-canonical-property"></a>PidLidAppointmentRecur 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)で指定されている定期的なパターンおよび範囲のいずれかを使用して、定期的なアイテムが発生する日付と時刻を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidapptrecur  <br/> |
|プロパティセット:  <br/> |PSETID_Appointment  <br/> |
|ロング ID (LID):  <br/> |0x00008216  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |カレンダー  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、定期的なアイテムのパターンと、 [[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)に詳細が記載されている範囲のいずれかを使用して、定期的なアイテムが発生する日付と時刻を指定します。 このプロパティの値には、変更済みおよび削除済みの両方の例外に関する情報も含まれています。日付、件名、場所など、例外の他のいくつかのプロパティなどの情報。 定期的な予定表アイテムのこのプロパティのバイナリデータは、 **AppointmentRecurrencePattern**構造体として格納されます。 このプロパティは、1つのインスタンスの予定表アイテムに存在してはなりません。 
  
次のようないくつかの制限があります。
  
- 複数のインスタンスを同じ日に開始することはできません。
    
- オカレンスは重複してはなりません。 具体的には、定期的なアイテムのインスタンスの開始日を変更する例外として、前のインスタンスが終了してから、定期的なアイテムの次のインスタンスの開始までの間に発生する必要があります。 定期的なアイテムの前または次のインスタンスが例外である場合も同様です。
    
定期的なアイテムのスケジュールは、定期的なパターンと範囲によって決まります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
[[OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> 電子メールおよびその他のオブジェクトの事前通知のプロパティと相互作用モデルを指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

