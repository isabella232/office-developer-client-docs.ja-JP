---
title: PidLidTaskStartDate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStartDate
api_type:
- COM
ms.assetid: fe87eb3d-21d1-45bb-b848-e141ce1be6a0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3bc475292e47a9ad8dd9565e17640ef95e7b3c76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316682"
---
# <a name="pidlidtaskstartdate-canonical-property"></a>PidLidTaskStartDate 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ユーザーがタスクを開始することを期待する日付。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidtaskstartdate  <br/> |
|プロパティセット:  <br/> |PSETID_Task  <br/> |
|ロング ID (LID):  <br/> |0x00008104  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>解説

このプロパティの値が設定されていない場合は、タスクに開始日がありません。 値 "0x5AE980E0" (1525252320) は、タスクに開始日が設定されていないことも意味します。 タスクの開始日が設定されている場合は、その値に午前0時の時間コンポーネントを指定し、 **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) および**dispidcommonstart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) プロパティも設定する必要があります。
  
このプロパティは、 [[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)にある情報フラグのプロトコル仕様とタスク関連のオブジェクトプロトコル仕様によって共有されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> 連絡先および個人用配布リストで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[PidLidTaskDueDate ���K���̃v���p�e�B](pidlidtaskduedate-canonical-property.md)
  
[PidLidCommonStart ���K���̃v���p�e�B](pidlidcommonstart-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

