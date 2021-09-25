---
title: PidLidTaskFCreator 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskFCreator
api_type:
- COM
ms.assetid: bb88750b-4773-4241-aa38-462a2634dbcb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dcbf11015dc4347a29620da003695b316e83cbbb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616692"
---
# <a name="pidlidtaskfcreator-canonical-property"></a>PidLidTaskFCreator 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
タスク要求を処理するのではなく、現在のユーザーまたはユーザー エージェントによって作成されたタスクを示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskFCreator  <br/> |
|プロパティ セット:  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x0000811E  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

クライアントは、ユーザーがタスクを作成するときにこのプロパティを TRUE に設定し、タスクが別のユーザーによって割り当てられている場合は FALSE に設定します。 このプロパティを設定しない場合は、TRUE の値が使用されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

