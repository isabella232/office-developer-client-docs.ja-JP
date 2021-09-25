---
title: '[ShapeShdwObliqueAngle] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033174
ms.localizationpriority: medium
ms.assetid: bad4c512-e91f-d459-d65c-a4ab725c3c14
description: 図形の斜体の影に角度を指定します。
ms.openlocfilehash: 504283783040899cf505498264b9a9c50c275f5e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553880"
---
# <a name="shapeshdwobliqueangle-cell-fill-format-section"></a>[ShapeShdwObliqueAngle] セル ([Fill Format] セクション)

図形の斜体の影に角度を指定します。
  
## <a name="remarks"></a>注釈

このセルの値がゼロ (0) の場合は影の傾きの角度が真上で、時計回りに角度を指定します。
  
この値は、[**影**] ダイアログ ボックスの [**方向**] 設定の値に対応しています (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**影**] をクリックし、[**影のオプション**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapeShdwObliqueAngle] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | ShapeShdwObliqueAngle  <br/> |
   
プログラムから、インデックスによって [ShapeShdwObliqueAngle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowFill** <br/> |
| セル インデックス:  <br/> |**visFillShdwObliqueAngle** <br/> |
   

