---
title: '[ShdwScaleFactor] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60083
localization_priority: Normal
ms.assetid: 10979706-6dfe-5241-e862-3f94716d14fa
description: 図形の影を拡大または縮小する割合を、パーセントで指定します。
ms.openlocfilehash: 9175e9a1148779524fdce96ff18eac22fe8dd421
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429006"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a>[ShdwScaleFactor] セル ([Page Properties] セクション)

図形の影を拡大または縮小する割合を、パーセントで指定します。 
  
## <a name="remarks"></a>注釈

各影には影付きのピン位置があります。これは、図形の pin に対応する影上の点です。 たとえば、図形のピンが図形の中央にある場合、影付きのピン位置は影の中心点になります。 単純な影に倍率を適用すると、倍率は、影付きのピン位置に揃えられます。斜体の影に倍率を適用すると、斜体の方向に倍率が適用されます。 
  
 このパーセンテージは、図形の影の種類が Page Default ([shapeshdwtype] cell が * * visFSTPageDefault * *) に設定されている場合に使用します。 
  
個々の図形に対してこの動作を設定するには、[Fill Format] セクションで [ShapeShdwScaleFactor] セルを使用します。
  
この値は、[**ページ設定**] ダイアログ ボックスの [**影**] タブにある [**倍率**] ボックスの値に対応しています (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックします)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwScaleFactor] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [shdwscalefactor]  <br/> |
   
プログラムから、インデックスによって [ShdwScaleFactor] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPage** <br/> |
| セル インデックス:  <br/> |**visPageShdwScaleFactor** <br/> |
   

