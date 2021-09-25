---
title: '[DontMoveChildren] セル ([Group Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm255
ms.localizationpriority: medium
ms.assetid: ff5bbf05-4851-30ce-7ee1-f0ce7b2781ab
description: グループ内の図形をマウスを使用してドラッグできるかどうかを指定します。
ms.openlocfilehash: 904d1cfceed285868279b8dafea6238eda0b638f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574364"
---
# <a name="dontmovechildren-cell-group-properties-section"></a>[DontMoveChildren] セル ([Group Properties] セクション)

グループ内の図形をマウスを使用してドラッグできるかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | グループ内の図形をマウスを使用してドラッグできません。  <br/> |
| FALSE  <br/> | グループ内の図形をマウスを使用してドラッグできます。  <br/> |
   
## <a name="remarks"></a>注釈

このセルの値が TRUE の場合でも、別の方法を使用してグループ内の図形を反転、回転、サイズ変更、位置変更することはできます。
  
Visio 2000 より前のバージョンの Visio で作成されたマスター シェイプのグループまたはマスター シェイプのインスタンスのグループの場合、このセルの値は TRUE に設定されます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DontMoveChildren] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | DontMoveChildren  <br/> |
   
プログラムから、インデックスによって [DontMoveChildren] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス :  <br/> |**visRowGroup** <br/> |
| セル インデックス:  <br/> |**visGroupDontMoveChildren** <br/> |
   

