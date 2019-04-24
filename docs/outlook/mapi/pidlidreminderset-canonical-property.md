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
ms.openlocfilehash: 59379b0b1345684a491f2f7f896f2b8fc8fd54c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335155"
---
# <a name="pidlidreminderset-canonical-property"></a>PidLidReminderSet 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通知がオブジェクトに設定されているかどうかを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidReminderSet  <br/> |
|プロパティセット:  <br/> |PSETID_Common  <br/> |
|ロング ID (LID):  <br/> |0x00008503  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |Reminder  <br/> |
   
## <a name="remarks"></a>解説

定期的な予定表オブジェクトがこのプロパティを TRUE に設定している場合、クライアントは例外に対してこの値を上書きできます。
  
定期的な予定表オブジェクトでこのプロパティを FALSE に設定すると、例外を含め、定期的なアイテム全体に対してアラームが無効になります。 定期的なタスクオブジェクトの場合、このプロパティは例外で無効にすることはできません (詳細については、「 [OXOCAL](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) 」および「 [OXOTASK](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) 」を参照してください)。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
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

