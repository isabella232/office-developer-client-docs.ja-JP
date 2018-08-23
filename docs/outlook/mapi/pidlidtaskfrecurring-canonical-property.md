---
title: PidLidTaskFRecurring 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFRecurring
api_type:
- COM
ms.assetid: 47c9ccbb-161c-4829-8ffb-201f3b54cd45
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 94ec76d3247421f163775245c43ee68e6f9b560b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569086"
---
# <a name="pidlidtaskfrecurring-canonical-property"></a>PidLidTaskFRecurring 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
タスクが定期的なパターンを含めるかどうかを示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskFRecur  <br/> |
|プロパティを設定します。  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008126  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティが未設定のままには、FALSE の既定値が使われます。 として**dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) のプロパティを設定する必要があります**dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) は TRUE に設定されている場合は、 [[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)で指定します。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

