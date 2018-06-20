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
ms.openlocfilehash: 99bc48f5332830512e1f5c2f6d93c70b67197c03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806458"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a>[ShdwScaleFactor] セル ([Page Properties] セクション)

図形の影を拡大または縮小する割合を、パーセントで指定します。 
  
## <a name="remarks"></a>注釈

各シャドウには、図形のピンに対応する影があり、影の pin 位置があります。 たとえば、図形の pin は図形の中央には、影の pin 位置は影の中央にポイントをします。 シンプルな影に縮尺を適用する、拡大率は、影の pin 位置に中心斜体の影に縮尺を適用する、斜めの方向に拡大率が適用されます。 
  
 図形の影の種類は、ページの既定値に設定されている場合は、このパーセンテージが使用される (ShapeShdwType のセルに等しい * * visFSTPageDefault * *)。 
  
個々の図形に対してこの動作を設定するには、[Fill Format] セクションで [ShapeShdwScaleFactor] セルを使用します。
  
この値は、[**ページ設定**] ダイアログ ボックスで [**影**] タブの [**倍率**] ボックスの値に対応して ([**デザイン**] タブで、矢印をクリック、 **[ページ設定**)。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShdwScaleFactor] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | ShdwScaleFactor  <br/> |
   
プログラムから、インデックスによって [ShdwScaleFactor] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPage** <br/> |
| セル インデックス:  <br/> |**visPageShdwScaleFactor** <br/> |
   

