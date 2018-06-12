---
title: '[DontMoveChildren] セル ([Group Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm255
localization_priority: Normal
ms.assetid: ff5bbf05-4851-30ce-7ee1-f0ce7b2781ab
description: グループ内の図形をマウスを使用してドラッグできるかどうかを指定します。
ms.openlocfilehash: df5d0d2b44e283ee8301d9c088d3ce55114e9a75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805257"
---
# <a name="dontmovechildren-cell-group-properties-section"></a>[DontMoveChildren] セル ([Group Properties] セクション)

グループ内の図形をマウスを使用してドラッグできるかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | グループ内の図形をマウスを使用してドラッグできません。  <br/> |
| FALSE  <br/> | グループ内の図形をマウスを使用してドラッグできます。  <br/> |
   
## <a name="remarks"></a>備考

このセルの値が TRUE の場合でも、別の方法を使用してグループ内の図形を反転、回転、サイズ変更、位置変更することはできます。
  
Visio 2000 より前のバージョンの Visio で作成されたマスター シェイプのグループまたはマスター シェイプのインスタンスのグループの場合、このセルの値は TRUE に設定されます。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[DontMoveChildren] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | DontMoveChildren  <br/> |
   
プログラムから、インデックスによって [DontMoveChildren] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowGroup** <br/> |
| セル インデックス:  <br/> |**visGroupDontMoveChildren** <br/> |
   

