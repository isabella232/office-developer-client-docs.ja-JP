---
title: PidLidTaskOrdinal 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskOrdinal
api_type:
- COM
ms.assetid: 1021860e-4c40-4c22-aa68-b568d046aaf7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c21826a5d9cdc7c2187c5866972109b396ea4919
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583675"
---
# <a name="pidlidtaskordinal-canonical-property"></a>PidLidTaskOrdinal 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
カスタムの並べ替えタスクを支援します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskOrdinal  <br/> |
|プロパティ セット:  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008123  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは未設定の場合があります。 設定する場合、その値は "0x800186A0" (-2,147,383,648) より大きく、"0x7FFE7960" (2,147,383,648) 未満で、同じフォルダー内のタスク間で一意である必要があります。
  
クライアントがフォルダーの **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) プロパティの現在の値の負の値より小さい数値にこのプロパティを設定するたびに、クライアントはフォルダーの **PR_ORDINAL_MOST** も更新する必要があります。 
  
フォルダー **PR_ORDINAL_MOST** プロパティを使用すると、同じフォルダー内のタスク間で一意の値を効率的に決定できます。 
  
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

