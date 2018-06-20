---
title: '[ReplaceLockShapeData] セル ([図形の動作の変更] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: マスター シェイプ内の指定したセルの値が図形の置換操作の実行中に置換される図形の値 (ローカル値を含む) を上書きするかどうかを示します。 ReplaceLockShapeData は、マスター シェイプの図形データが置換される図形の図形データのすべてを上書きしているかどうかを決定します。
ms.openlocfilehash: 07547140c7c96e49663270e51a90fd559afedf29
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806224"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a>[ReplaceLockShapeData] セル ([図形の動作の変更] セクション)

マスター シェイプ内の指定したセルの値が図形の置換操作の実行中に置換される図形の値 (ローカル値を含む) を上書きするかどうかを示します。 **ReplaceLockShapeData**は、マスター シェイプの図形データが置換される図形の図形データのすべてを上書きしているかどうかを決定します。 
  
|**値**|**説明**|
|:-----|:-----|
|1 (TRUE)  <br/> |置換後の図形の上にすべての行と、マスター シェイプの**図形データ**セクションの値がコピーされ、古いに置き換えられた図形からすべてのローカル値が破棄されます。  <br/> |
|0 (FALSE)  <br/> |行とマスター シェイプの**図形データ**セクションの値は、置換後の図形にコピーされます。 置換後の図形には、ローカルの値を持つ古い図形の**図形データ**セクションの行が転送されます。  <br/> |
   
## <a name="remarks"></a>備考

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **ReplaceLockShapeData** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ReplaceLockShapeData  <br/> |
   
プログラムから、インデックスによって [ **ReplaceLockShapeData** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowReplaceBehaviors** <br/> |
| セル インデックス:  <br/> |**visReplaceLockShapeData** <br/> |
   

