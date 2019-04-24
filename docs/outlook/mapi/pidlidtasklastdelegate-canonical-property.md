---
title: PidLidTaskLastDelegate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastDelegate
api_type:
- COM
ms.assetid: 5eb8c1ce-063f-4273-acba-e6f9c994e7d3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ddf4b81ed35f500dad0029ea6375e9a75a996186
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355672"
---
# <a name="pidlidtasklastdelegate-canonical-property"></a>PidLidTaskLastDelegate 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 タスクを最後に割り当てたユーザーまたは割り当てられたユーザーの名前を指定します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidtasklastdelegate  <br/> |
|プロパティセット:  <br/> |PSETID_Task  <br/> |
|ロング ID (LID):  <br/> |0x00008125  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>解説

タスクの要求を送信する前に、クライアントはこのプロパティをタスク assigner の名前に設定します。 タスクの応答を送信する前に、クライアントはこのプロパティをタスクの実施者の名前に設定します。
  
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

