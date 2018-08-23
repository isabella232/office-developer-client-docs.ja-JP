---
title: PidLidReminderSet 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderSet
api_type:
- COM
ms.assetid: 06b7792c-1b43-4e20-9a3b-44f2664b2125
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c056b0e587de06f6c32ceb3cebbb96f2fb737208
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579082"
---
# <a name="pidlidreminderset-canonical-property"></a>PidLidReminderSet 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
オブジェクトにアラームを設定するかどうかを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidReminderSet  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x00008503  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |Reminder  <br/> |
   
## <a name="remarks"></a>注釈

定期的な予定表オブジェクトにこのプロパティを TRUE に設定がある場合、クライアントは例外の値をオーバーライドできます。
  
このプロパティが FALSE の場合の例外を含め、シリーズ全体での定期的な予定表オブジェクトでアラームが無効になります。 定期的なタスクは、オブジェクトの例外が (詳細については、 [[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)と[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)を参照) でこのプロパティをオーバーライドできません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> 電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

