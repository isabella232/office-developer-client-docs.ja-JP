---
title: PidLidToDoSubOrdinal 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidToDoSubOrdinal
api_type:
- COM
ms.assetid: e3bc15ef-155e-49fd-88e5-64713df9b939
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7add56dc1953e06a9842a6412f103c073bc75da8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579342"
---
# <a name="pidlidtodosubordinal-canonical-property"></a>PidLidToDoSubOrdinal 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**dispidToDoOrdinalDate** [(PidLidToDoOrdinalDate)](pidlidtodoordinaldate-canonical-property.md)プロパティがオブジェクトを並べ替え、その結果をタイに並べ替える場合、タイ ブレーカーとして機能します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidToDoSubOrdinal  <br/> |
|プロパティ セット:  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x000085A1  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

使用する場合、このプロパティは辞書的に並べ替える必要があります。 文字列のコンポーネント文字は、0 から 9 の数字で構成する必要があります。 このプロパティは、最初は "5555555" に設定する必要があります。 このプロパティの長さは、254 文字 (終端の NULL 文字を除く) を超えることはできません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> フラグに関連するプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[PidLidToDoOrdinalDate 標準プロパティ](pidlidtodoordinaldate-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

