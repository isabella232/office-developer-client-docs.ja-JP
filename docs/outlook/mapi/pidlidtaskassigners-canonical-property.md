---
title: PidLidTaskAssigners 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigners
api_type:
- COM
ms.assetid: 07500bd0-bcff-4b03-8ed3-80508875e253
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 97a4915d5422f6c5463ed399835172725b83407f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303067"
---
# <a name="pidlidtaskassigners-canonical-property"></a>PidLidTaskAssigners 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
タスク割り当て者を表すエントリのスタックが含まれる。 最新のタスク割り当て者がスタックの上部に表示されます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskMyDelegators  <br/> |
|プロパティ セット:  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008117  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

クライアントはタスク要求を受信すると、このプロパティに追加されます。このプロパティには、タスクの送信者を表すエントリである [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)で定義されている構造が追加されます。 クライアントがタスク拒否を受け取った場合、クライアントは最後のタスク割り当て者エントリをこのプロパティから削除します。 クライアントがタスク応答を送信すると、クライアントは、このプロパティの値にリストされている最後のタスク割り当て者に送信します。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> タスク、タスクの割り当て、およびタスクの更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。 
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

