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
ms.openlocfilehash: db94d68a01b65410cf4f3f1f461c780f2bb01918
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568533"
---
# <a name="pidlidtasklastuser-canonical-property"></a>PidLidTaskLastUser 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
最新のユーザーがタスクの所有者の名前を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskLastUser  <br/> |
|プロパティを設定します。  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008122  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

クライアントでは、仕事の依頼を送信する前に、仕事のタスクを割り当てた人の名前にこのプロパティを設定します。 クライアントでは、仕事の承諾を送信する前に、タスク実施者の名前にこのプロパティを設定します。 クライアントは、タスクの辞退を送信する前に、仕事のタスクを割り当てた人の名前にこのプロパティを設定します。
  
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

