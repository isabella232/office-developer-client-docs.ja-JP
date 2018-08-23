---
title: PidLidTaskAccepted 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAccepted
api_type:
- COM
ms.assetid: 8e31f893-b639-43da-a535-662153c82d82
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 08ea83a12b1c5751ed66643eaacd9bbdd261ff19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579005"
---
# <a name="pidlidtaskaccepted-canonical-property"></a>PidLidTaskAccepted 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
タスクの実施者が仕事の依頼に返信されているかどうかを示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskAccepted  <br/> |
|プロパティを設定します。  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008108  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

クライアントは、タスクには、FALSE にこのプロパティを設定またはタスクが承諾または却下すると、クライアントが TRUE にこのプロパティを設定します。 プロパティが未設定のままには、FALSE の値が使われます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> プロパティは、連絡先、個人用配布リストの許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

