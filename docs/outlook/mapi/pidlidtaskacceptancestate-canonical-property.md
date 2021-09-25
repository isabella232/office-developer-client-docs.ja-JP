---
title: PidLidTaskAcceptanceState 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskAcceptanceState
api_type:
- COM
ms.assetid: 7012f524-bc66-48ea-85b5-163e05029d35
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bcd1e034e22ff4a075e089fda0dbebd4e7a7d4a3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591732"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a>PidLidTaskAcceptanceState 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
タスクの受け入れ状態を示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskDelegValue  <br/> |
|プロパティ セット:  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x0000812A  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

次の表に、このプロパティで使用できる値を示します。
  
|**値**|**説明**|
|:-----|:-----|
|0x00000000  <br/> |タスクが割り当てられていない。  <br/> |
|0x00000001  <br/> |タスクの受け入れ状態が不明です。  <br/> |
|0x00000002  <br/> |タスクの割り当て先がタスクを承諾しました。 この値は、クライアントがタスクの受け入れを処理するときに設定されます。  <br/> |
|0x00000003  <br/> |タスクの割り当て先がタスクを拒否しました。 この値は、クライアントがタスクの拒否を処理するときに設定されます。  <br/> |
   
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

