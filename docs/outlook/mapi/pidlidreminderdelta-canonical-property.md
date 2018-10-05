---
title: PidLidReminderDelta 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderDelta
api_type:
- COM
ms.assetid: 011d73d0-8b38-4a4e-a56f-92dec451946a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 86a0203f930661452bb143e247c17ef6da8ed436
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398005"
---
# <a name="pidlidreminderdelta-canonical-property"></a>PidLidReminderDelta 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アラームが最初に期限切れの時刻と開始時刻、カレンダー オブジェクトの間隔を分単位で間隔を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidReminderDelta  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x00008501  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |Reminder  <br/> |
   
## <a name="remarks"></a>備考

カレンダー オブジェクトに対してこのプロパティを設定する必要があります。 以外のカレンダーのすべてのオブジェクトに対してこのプロパティが"0x00000000"に設定する必要がありますされ、無視されます。 定期的な予定表オブジェクトのインスタンスが 1 つのアラームが消去されたとき、このプロパティの値は次のインスタンスをシグナルの時間の計算に使用されます。 カレンダー オブジェクトの作成の詳細については、 [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)を参照してください。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> 電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

