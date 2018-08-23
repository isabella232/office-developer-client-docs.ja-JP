---
title: PidLidToDoSubOrdinal 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoSubOrdinal
api_type:
- COM
ms.assetid: e3bc15ef-155e-49fd-88e5-64713df9b939
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 98dfdab24d2c4170609d9db1c3104a3f17436736
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578067"
---
# <a name="pidlidtodosubordinal-canonical-property"></a>PidLidToDoSubOrdinal 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
**DispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) のプロパティがオブジェクトと同数の結果をソートするときは、リンク付けブレーカーとして機能します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidToDoSubOrdinal  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x000085A1  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

使用する場合は、このプロパティを辞書順に並べ替える必要があります。 文字列のコンポーネントの文字は必要がありますのみの数字 0 から 9 までので構成されます。 「5555555」に、このプロパティ最初に設定する必要があります。 このプロパティの長さは、254 文字まで (終端の NULL 文字を除く) を超えない必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> プロパティ フラグに関連する操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[PidLidToDoOrdinalDate 標準プロパティ](pidlidtodoordinaldate-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

