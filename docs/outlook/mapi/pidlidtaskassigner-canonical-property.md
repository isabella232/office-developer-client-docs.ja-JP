---
title: PidLidTaskAssigner 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskAssigner
api_type:
- COM
ms.assetid: f7047e4e-0fb3-476b-9568-8f1135e6d970
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0c93afbd8634b0c6c5653f447593e089f569625b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555560"
---
# <a name="pidlidtaskassigner-canonical-property"></a>PidLidTaskAssigner 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 タスクが最後に割り当てられたユーザーの名前を指定します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskDelegator  <br/> |
|プロパティ セット:  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008121  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

タスクが割り当てられていない場合、このプロパティは未設定の残りになります。 タスクの割り当て先がタスク要求を受け取った後、クライアントはこのプロパティを設定します。このプロパティはタスクの割り当て先のコピーでは設定されない。 クライアントが **dispidTaskMyDelegators** [(PidLidTaskAssigners)](pidlidtaskassigners-canonical-property.md)プロパティのタスク割り当て者リストにタスク割り当て者を追加または削除する場合は **、dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) プロパティを追加または削除したタスク割り当て者に設定する必要があります。
  
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

