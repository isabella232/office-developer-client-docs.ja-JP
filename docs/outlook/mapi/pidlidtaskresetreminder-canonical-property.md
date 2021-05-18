---
title: PidLidTaskResetReminder 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskResetReminder
api_type:
- COM
ms.assetid: f6da69ff-a913-4a65-bb07-8ad3c5685e5e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9a438fb2b1862d44905a63fda3e5f68b7878cd99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316619"
---
# <a name="pidlidtaskresetreminder-canonical-property"></a>PidLidTaskResetReminder 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) が FALSE である場合でも、定期的なタスクの今後のインスタンスにリマインダーが必要かどうかを示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskResetReminder  <br/> |
|プロパティ セット:  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008107  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

この値は、タスクのアラームが閉じらされた場合は TRUE に設定され、それ以外の場合は FALSE に設定されます。 設定を解除した場合、既定の FALSE が使用されます。
  
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)で指定されている通り **、dispidReminderSet** プロパティは、タスクにアラームが設定されているかどうかを示します。 ただし、このプロパティは、1 つのタスクにアラームが存在するのみを示します。 定期的なタスクの将来のインスタンスにリマインダーが必要かどうかを判断するために単独で使用することはできません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> メールなどのオブジェクトアラームのプロパティと対話モデルを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[PidLidReminderSet ���K���̃v���p�e�B](pidlidreminderset-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

