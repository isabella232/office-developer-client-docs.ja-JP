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
ms.openlocfilehash: 5862b61ca1f5df25ca97bf8742b9e20bf45091a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436266"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a>[ShapeShdwScaleFactor] セル ([Fill Format] セクション)

図形の影を拡大または縮小できる割合を、パーセントで指定します。
  
## <a name="remarks"></a>注釈

各シャドウには影付きピンの位置があります。これは、図形のピンに対応するシャドウ上のポイントです。 たとえば、図形のピンが図形の中央にある場合、影付きピンの位置は影の中心のポイントになります。 単純な影にスケールを適用する場合、倍率は影付きピンの位置の中央に配置されます。斜めの影にスケールを適用すると、斜め方向に倍率が適用されます。 
  
この値をページのすべての図形に設定するには、[Page Properties] セクションで [ShdwScaleFactor] セルを使用します。
  
この値は、[**影**] ダイアログ ボックスの [**倍率**] 設定の値に対応しています (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**影**] をクリックして、[**影のオプション**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapeShdwScaleFactor] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |ShapeShdwScaleFactor  <br/> |
   
プログラムから、インデックスによって [ShapeShdwScaleFactor] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowFill** <br/> |
|セル インデックス:  <br/> |**visFillShdwScaleFactor** <br/> |
   

