---
title: PidLidTaskAccepted 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskAccepted
api_type:
- COM
ms.assetid: 8e31f893-b639-43da-a535-662153c82d82
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 45f745eb32e6b52b271d05cf3a89f2e645b9feb6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630202"
---
# <a name="pidlidtaskaccepted-canonical-property"></a>PidLidTaskAccepted 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
タスクの割り当て先がタスク要求に返信したかどうかを示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskAccepted  <br/> |
|プロパティ セット:  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008108  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

クライアントは、新しいタスクに対してこのプロパティを FALSE に設定するか、タスクが受け入れられるか拒否された場合に、このプロパティを TRUE に設定します。 プロパティが設定されていない場合は、FALSE の値が使用されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> 連絡先と個人用配布リストで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

