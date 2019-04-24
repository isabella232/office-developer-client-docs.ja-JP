---
title: PidLidTaskHistory 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskHistory
api_type:
- COM
ms.assetid: 104ef21c-b607-48b7-9b06-bc53b7d9b68a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 39f2e6aeb4026f0b33be08b3bd8123283e5df3e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303011"
---
# <a name="pidlidtaskhistory-canonical-property"></a>PidLidTaskHistory 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
タスクに対して最後に行った変更の種類を示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskHistory  <br/> |
|プロパティセット:  <br/> |PSETID_Task  <br/> |
|ロング ID (LID):  <br/> |0x0000811A  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>解説

このプロパティの値が設定されている場合は、 **dispidtasklastupdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) プロパティも現在の時刻に設定する必要があります。 次の表に、 **dispidTaskHistory**プロパティの値を、優先度の高い順に示します。 
  
|**値**|**説明**|
|:-----|:-----|
|0x00000004  <br/> |**dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) プロパティが変更されました。  <br/> |
|0x00000003  <br/> |別のプロパティが変更されました。  <br/> |
|0x00000001  <br/> |タスクの実施者がこのタスクを承諾しました。  <br/> |
|0x00000002  <br/> |タスクの実施者がこのタスクを拒否しました。  <br/> |
|0x00000005  <br/> |タスクは、タスクの担当者に割り当てられました。  <br/> |
|0x00000000  <br/> |変更は行われませんでした。  <br/> |
   
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

