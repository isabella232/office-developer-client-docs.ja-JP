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
ms.openlocfilehash: b1b18db072cb7c62c10c8ee4ab79dd1d8754388f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588021"
---
# <a name="pidlidclipend-canonical-property"></a>PidLidClipEnd 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
カレンダー オブジェクトのインスタンスを 1 つのイベントの終了日時に世界協定時刻 (UTC) を指定します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidClipEnd  <br/> |
|プロパティを設定します。  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008236  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|領域:  <br/> |予定表  <br/> |
   
## <a name="remarks"></a>注釈

カレンダー オブジェクトのインスタンスを 1 つのイベントの終了日時を UTC で指定します。 定期的な一連のこのプロパティを指定の午前 0 時 (UTC) での定期的な系列の最後のインスタンスの日付に定期的に終了すると、大文字と小文字の値が 31 年 8 月をする必要がありますがあるない場合を除き、4500、午後 11 時 59 分
  
このプロパティの値は、 **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) の値に設定する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
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

