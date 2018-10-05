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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383528"
---
# <a name="pidlidtaskstartdate-canonical-property"></a>PidLidTaskStartDate 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ユーザーがタスクを開始するのには必要とする日付です。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskStartDate  <br/> |
|プロパティを設定します。  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008104  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>備考

このプロパティの値が未設定のままである場合、タスクには開始日はありません。 "0x5AE980E0"(1,525,252,320) の値は、タスクに開始日がないことも意味します。 タスクに開始日がある場合は、値が午前 0 時という時刻成分を持つ必要があり、 **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) と**dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) のプロパティを設定もする必要があります。
  
情報フラグを設定するプロトコルの仕様でこのプロパティを共有し、Task-Related オブジェクトのプロトコル仕様は、 [[MS OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)にあります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> 連絡先と個人用配布リストで許可されている操作のプロパティを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[PidLidTaskDueDate ���K���̃v���p�e�B](pidlidtaskduedate-canonical-property.md)
  
[PidLidCommonStart ���K���̃v���p�e�B](pidlidcommonstart-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

