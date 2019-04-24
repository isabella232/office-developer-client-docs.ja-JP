---
title: PidLidTaskLastUser 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastUser
api_type:
- COM
ms.assetid: 914c55e9-cb36-46a4-b5ee-382413fa25f9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 76311a76001b122bdfd984b9dedc37c2ff878fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360446"
---
# <a name="pidlidtasklastuser-canonical-property"></a>PidLidTaskLastUser 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
タスクの所有者である最新のユーザーの名前を示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidtasklastuser  <br/> |
|プロパティセット:  <br/> |PSETID_Task  <br/> |
|ロング ID (LID):  <br/> |0x00008122  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>解説

クライアントは、タスク要求を送信する前に、このプロパティをタスク assigner の名前に設定します。 クライアントは、タスクの承諾を送信する前に、タスクの割り当て先の名前にこのプロパティを設定します。 クライアントがタスク拒否を送信する前に、このプロパティはタスク assigner の名前に設定されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> タスク、タスクの割り当て、およびタスクの更新に相当する電子メールをモデル化する複数のオブジェクトを定義します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

