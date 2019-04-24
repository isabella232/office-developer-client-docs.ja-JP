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
ms.openlocfilehash: 2b15d75a98b5f5a72bce8b80758d27b197a346ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338585"
---
# <a name="dontmovechildren-cell-group-properties-section"></a>[DontMoveChildren] セル ([Group Properties] セクション)

グループ内の図形をマウスを使用してドラッグできるかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | グループ内の図形をマウスを使用してドラッグできません。  <br/> |
| FALSE  <br/> | グループ内の図形をマウスを使用してドラッグできます。  <br/> |
   
## <a name="remarks"></a>解説

このセルの値が TRUE の場合でも、別の方法を使用してグループ内の図形を反転、回転、サイズ変更、位置変更することはできます。
  
Visio 2000 より前のバージョンの Visio で作成されたマスター シェイプのグループまたはマスター シェイプのインスタンスのグループの場合、このセルの値は TRUE に設定されます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DontMoveChildren] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [dontmovechildren]  <br/> |
   
プログラムから、インデックスによって [DontMoveChildren] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス :  <br/> |**visRowGroup** <br/> |
| セル インデックス:  <br/> |**visGroupDontMoveChildren** <br/> |
   

