---
title: PidLidClipEnd 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidClipEnd
api_type:
- COM
ms.assetid: 17c8db96-80dd-4a7a-9a1b-ab1b37ba616c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 71a0a50f26b26d65ed34f38c2a0c7f930e6082a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349183"
---
# <a name="pidlidclipend-canonical-property"></a>PidLidClipEnd 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
単一インスタンスの予定表オブジェクトの、世界協定時刻 (UTC) でのイベントの終了日時を指定します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidclipend  <br/> |
|プロパティセット:  <br/> |PSETID_Appointment  <br/> |
|ロング ID (LID):  <br/> |0x00008236  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |カレンダー  <br/> |
   
## <a name="remarks"></a>解説

単一インスタンスの calendar オブジェクトの場合は、イベントの終了日時を UTC で指定します。 定期的なアイテムの場合、このプロパティは定期的なアイテムの最後のインスタンスの日付の午前0時を指定します。この場合、定期的なアイテムの最後のインスタンスの日付は7月31日である必要があります。
  
このプロパティの値には、 **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) の値を設定する必要があります。
  
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

