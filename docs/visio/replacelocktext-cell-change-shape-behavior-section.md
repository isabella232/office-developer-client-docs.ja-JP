---
title: '[ReplaceLockText] セル ([図形の動作の変更] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: マスター シェイプ内の指定したセルの値が図形の置換操作の実行中に置換される図形の値 (ローカル値を含む) を上書きするかどうかを示します。 ReplaceLockText は、マスター上に表示されるテキストが置換される図形のテキストを上書きするかどうかを決定します。
ms.openlocfilehash: 75fb0831e7361345f04d7912eb0a55959d9417cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806235"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a>[ReplaceLockText] セル ([図形の動作の変更] セクション)

マスター シェイプ内の指定したセルの値が図形の置換操作の実行中に置換される図形の値 (ローカル値を含む) を上書きするかどうかを示します。 **ReplaceLockText**は、マスター上に表示されるテキストが置換される図形のテキストを上書きするかどうかを決定します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> | マスター シェイプのテキストは、古い図形のテキストに優先します。さらに、マスター シェイプは、図形の置換操作中、次のセクション内のセルの値に優先します。<br/> **テキスト フィールド**] セクション  <br/> **テキスト ブロックの書式**セクション  <br/> |
|FALSE  <br/> |置換後の図形には、その図形に追加された、古い図形からのテキスト、テキスト フィールド、またはその他のテキスト プロパティが格納されます。  <br/> 置換後の図形には、古い図形からテキストのプロパティが含まれている、置換後の図形も値があります、**文字**および**段落**の前のセクションから 1 つ以上の行がある場合。  <br/> |
   
TRUE (1) に設定されると、マスター シェイプの値が、置換される図形の次の値に置換されます。
  
- [[TheText] セル ([Events] セクション)](thetext-cell-events-section.md)
    
- [[Character] セクション](character-section.md)内のセル
    
- [[Paragraph] セクション](paragraph-section.md)内のセル
    
- [[Tabs] セクション](tabs-section.md)内のセル
    
## <a name="remarks"></a>備考

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **ReplaceLockText** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ReplaceLockText  <br/> |
   
プログラムから、インデックスによって [ **ReplaceLockText** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowReplaceBehaviors** <br/> |
| セル インデックス:  <br/> |**visReplaceLockText** <br/> |
   

