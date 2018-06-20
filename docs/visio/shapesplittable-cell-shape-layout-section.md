---
title: '[ShapeSplittable] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60081
localization_priority: Normal
ms.assetid: 6330304a-71f3-62b4-1b27-14495e3f12c3
description: この 1 次元図形が分割可能かどうかを示します。
ms.openlocfilehash: e2db881465a19b34d5788f1621f15c4d7d15c293
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806435"
---
# <a name="shapesplittable-cell-shape-layout-section"></a>[ShapeSplittable] セル ([Shape Layout] セクション)

この 1 次元図形が分割可能かどうかを示します。 
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | この図形は分割できません。  <br/> |**visSLOSplittableNone** <br/> |
| 1  <br/> | この図形は分割できます。  <br/> |**visSLOSplittableAllow** <br/> |
   
## <a name="remarks"></a>注釈

コネクタと他の 1 次元図形に対する既定の動作は、図面の種類によって異なります。 
  
図形の自動分割は、アプリケーション、ページ、および図形の 3 つのレベルで有効または無効にできます。既定では、アプリケーション レベルとページ レベルで分割できます。 
  
アプリケーション レベルで分割を無効にするを有効または、 **Visio のオプション**] ダイアログ ボックスの [**詳細設定**] タブに**コネクタ分割を有効にする**設定を使用して、([**ファイル**] タブをクリックして、**オプション**] をクリックし、 **高度な**)。 
  
ページの分割を無効にするを有効または、 [PageShapeSplit](pageshapesplit-cell-page-layout-section.md)のセルを参照してください。 
  
1 次元の分割可能図形を分割できる図形には、 [[shapesplit]](shapesplit-cell-shape-layout-section.md)セルを参照してください。 
  
取得する、[ShapeSplittable] セルへの参照名で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ShapeSplittable  <br/> |
   
プログラムから、インデックスによって [ShapeSplittable] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowShapeLayout** <br/> |
| セル インデックス:  <br/> |**visSLOSplittable** <br/> |
   

