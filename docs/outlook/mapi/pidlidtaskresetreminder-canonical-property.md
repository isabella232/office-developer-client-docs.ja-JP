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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9a438fb2b1862d44905a63fda3e5f68b7878cd99
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384956"
---
# <a name="pidlidtaskresetreminder-canonical-property"></a>PidLidTaskResetReminder 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**DispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) が FALSE である場合でも、定期的な仕事の将来のインスタンスに通知が必要なかどうかを示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskResetReminder  <br/> |
|プロパティを設定します。  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008107  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>備考

タスクのアラームを閉じる、およびそれ以外の場合は FALSE に設定すると、この値は TRUE に設定します。 未設定のままに、既定値は FALSE と見なされます。
  
[[MS OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)で指定したとは、 **dispidReminderSet**プロパティは、タスクにアラームを設定するかどうかを示します。 ただし、このプロパティには、1 つのタスクにアラームが存在することだけを示します。 アラームが定期的な仕事の将来のインスタンスに必要があるかどうかを確認するには、単独で使用できません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。
    
[[MS OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> 電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[PidLidReminderSet ���K���̃v���p�e�B](pidlidreminderset-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

