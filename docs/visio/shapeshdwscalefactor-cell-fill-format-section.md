---
title: '[ShapeShdwScaleFactor] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033175
localization_priority: Normal
ms.assetid: 94ec06c5-8d2f-dd27-1eed-1abaf93daba8
description: 図形の影を拡大または縮小できる割合を、パーセントで指定します。
ms.openlocfilehash: 0b6392030e7efc8ea36c8d728b99c9b82482840b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806438"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a>[ShapeShdwScaleFactor] セル ([Fill Format] セクション)

図形の影を拡大または縮小できる割合を、パーセントで指定します。
  
## <a name="remarks"></a>注釈

各シャドウには、図形のピンに対応する影があり、影の pin 位置があります。 たとえば、図形の pin は図形の中央には、影の pin 位置は影の中央にポイントをします。 シンプルな影に縮尺を適用する、拡大率は、影の pin 位置に中心斜体の影に縮尺を適用する、斜めの方向に拡大率が適用されます。 
  
この値をページのすべての図形に設定するには、[Page Properties] セクションで [ShdwScaleFactor] セルを使用します。
  
この値は、[**影**] ダイアログ ボックスで**表示倍率**の設定の値に対応 ([**ホーム**] タブの [**図形**] グループで、**シャドウ**] をクリックし、[**影のオプション**] をクリック) します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShapeShdwScaleFactor] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |ShapeShdwScaleFactor  <br/> |
   
プログラムから、インデックスによって [ShapeShdwScaleFactor] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowFill** <br/> |
|セル インデックス:  <br/> |**visFillShdwScaleFactor** <br/> |
   

