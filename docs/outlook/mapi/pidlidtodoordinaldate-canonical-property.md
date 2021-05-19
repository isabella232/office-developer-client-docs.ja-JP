---
title: PidLidToDoOrdinalDate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoOrdinalDate
api_type:
- COM
ms.assetid: b6a500fc-07f4-4788-ae46-d179a96a48e2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b0c5e3019efeeb0b9788d81e8730e976bfcc9d75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345277"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a>PidLidToDoOrdinalDate 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
統合 To Do リスト内のオブジェクトの並べ替え順序を決定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidToDoOrdinalDate  <br/> |
|プロパティ セット:  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x000085A0  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

オブジェクトにフラグが設定されている場合、このプロパティは協定世界時 (UTC) の現在の時刻に設定する必要があります。 
  
クライアントがユーザーがドラッグなどのメカニズムを使用して統合タスク リスト内のタスクを並べ替える場合、適切なアルゴリズムを使用してこのプロパティの新しい値を決定し、このプロパティを並べ替えフィールドとして使用するときにタスクが正しい場所に表示されます。
  
このプロパティを使用してオブジェクトを並べ替え、並べ替えを行った結果がタイの場合 **、dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) プロパティがタイ ブレーカーとして使用されます。
  
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



[PidLidToDoSubOrdinal 標準プロパティ](pidlidtodosubordinal-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

