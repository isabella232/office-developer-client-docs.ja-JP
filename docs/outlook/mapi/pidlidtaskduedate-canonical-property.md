---
title: PidLidTaskDueDate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskDueDate
api_type:
- COM
ms.assetid: 69ed3d48-3741-4a9a-8f98-51382b850c27
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f163fbd80ebe6cf60c50929585995053473d377b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555518"
---
# <a name="pidlidtaskduedate-canonical-property"></a>PidLidTaskDueDate 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ユーザーがタスクを完了する予定の日付を表します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskDueDate  <br/> |
|プロパティ セット:  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008105  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの設定が解除または設定されている場合、タスクに期限はありません (1,525,252,320 0x5AE980E0) ただし、期限は **、dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) プロパティに開始日が指定されている場合にのみ省略できます。 タスクに期日がある場合、値には午前 0 時の時刻コンポーネントが必要で **、dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) プロパティも設定する必要があります。 **dispidTaskStartDate** に開始日がある場合 **、dispidTaskDueDate** プロパティの値は **、dispidTaskStartDate** の値以上である必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> メールなどのオブジェクトアラームのプロパティと対話モデルを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

