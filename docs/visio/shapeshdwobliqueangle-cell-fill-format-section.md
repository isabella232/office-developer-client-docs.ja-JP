---
title: '[ShapeShdwObliqueAngle] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033174
localization_priority: Normal
ms.assetid: bad4c512-e91f-d459-d65c-a4ab725c3c14
description: 図形の斜体の影に角度を指定します。
ms.openlocfilehash: 005415e497a4d985d3fb8ec70d62ba40d9e80c91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349195"
---
# <a name="shapeshdwobliqueangle-cell-fill-format-section"></a>[ShapeShdwObliqueAngle] セル ([Fill Format] セクション)

図形の斜体の影に角度を指定します。
  
## <a name="remarks"></a>解説

このセルの値がゼロ (0) の場合は影の傾きの角度が真上で、時計回りに角度を指定します。
  
この値は、[**影**] ダイアログ ボックスの [**方向**] 設定の値に対応しています (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**影**] をクリックし、[**影のオプション**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapeShdwObliqueAngle] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [shapeshdwobliqueangle]  <br/> |
   
プログラムから、インデックスによって [ShapeShdwObliqueAngle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowFill** <br/> |
| セル インデックス:  <br/> |**visFillShdwObliqueAngle** <br/> |
   

