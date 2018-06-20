---
title: PidLidToDoOrdinalDate の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d708424ccb15be15746fe8a33eea73a8e0f99323
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802253"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a>PidLidToDoOrdinalDate の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
統合の to do リスト内のオブジェクトの並べ替え順序を決定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidToDoOrdinalDate  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x000085A0  <br/> |
|データを入力します。  <br/> |PT_SYSTIME  <br/> |
|領域:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>備考

オブジェクトのフラグを設定すると、現在の時刻を世界協定時刻 (UTC) でこのプロパティを設定する必要があります。 
  
Sor としてこのプロパティを使用する場合、適切な場所にタスクが表示されるようにこのプロパティの新しい値を決定するのに、適切なアルゴリズムを使用できるクライアントでは、ドラッグを使用して統合タスク ・ リストまたはその他の機構内のタスクの順序を変更するのにユーザーを許可している場合残ったフィールドです。
  
オブジェクトと同数の並べ替えの結果を並べ替えるには、このプロパティを使用する場合、 **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) のプロパティは、リンク付けブレーカーとして使用されます。
  
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



[PidLidToDoSubOrdinal の標準的なプロパティ](pidlidtodosubordinal-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

