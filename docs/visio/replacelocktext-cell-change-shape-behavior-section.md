---
title: '[ReplaceLockText] セル ([図形の動作の変更] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: マスター シェイプ内の指定したセルの値が、図形の置換操作中に置換される値 (ローカル値を含む) に優先するかどうかを示します。ReplaceLockText は、マスターに表示されるテキストが、置換される図形のテキストに優先するかを決定します。
ms.openlocfilehash: f0ddee2e50750ec91c811d409d507767258f45f4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570184"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a>[ReplaceLockText] セル ([図形の動作の変更] セクション)

マスター シェイプ内の指定したセルの値が、図形の置換操作中に置換される値 (ローカル値を含む) に優先するかどうかを示します。**ReplaceLockText** は、マスターに表示されるテキストが、置換される図形のテキストに優先するかを決定します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> | マスター シェイプのテキストは、古い図形のテキストに優先します。さらに、マスター シェイプは、図形の置換操作中、次のセクション内のセルの値に優先します。<br/> [**テキスト フィールド**] セクション  <br/> [**テキスト ブロックの形式**] セクション  <br/> |
|FALSE  <br/> |置換後の図形には、その図形に追加された、古い図形からのテキスト、テキスト フィールド、またはその他のテキスト プロパティが格納されます。  <br/> 置換後の図形に古い図形からのテキスト プロパティが格納されている場合、置換後の図形には、古い図形の [**文字**] セクションと [**段落**] セクションに複数の行が存在すると、それらの値も格納されます。  <br/> |
   
TRUE (1) に設定されると、マスター シェイプの値が、置換される図形の次の値に置換されます。
  
- [[TheText] セル ([Events] セクション)](thetext-cell-events-section.md)
    
- [[文字] セクション](character-section.md) のセル
    
- [[段落] セクション](paragraph-section.md) のセル
    
- [[タブ] セクション](tabs-section.md) のセル
    
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**ReplaceLockText**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ReplaceLockText  <br/> |
   
プログラムから、インデックスによって [**ReplaceLockText**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowReplaceBehaviors** <br/> |
| セル インデックス:  <br/> |**visReplaceLockText** <br/> |
   

