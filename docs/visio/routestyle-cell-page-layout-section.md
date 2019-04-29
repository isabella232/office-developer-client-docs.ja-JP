---
title: '[RouteStyle] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251662
localization_priority: Normal
ms.assetid: 3a223dac-538b-cb5d-a32d-61395276f9da
description: ローカルな迂回方法を持たない図面ページ上のすべてのコネクタに対して、迂回方法と方向を指定します。
ms.openlocfilehash: 38de871460c155ee5d495599a239ebeb0ff1c33d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424785"
---
# <a name="routestyle-cell-page-layout-section"></a>[RouteStyle] セル ([Page Layout] セクション)

ローカルな迂回方法を持たない図面ページ上のすべてのコネクタに対して、迂回方法と方向を指定します。
  
|**値**|**迂回方法**|**Direction**|**オートメーション定数**|
|:-----|:-----|:-----|:-----|
|.0  <br/> |直角 (既定値)  <br/> |なし  <br/> |**visLORouteDefault** <br/> |
|1   <br/> |直角  <br/> |なし  <br/> |**visLORouteRightAngle** <br/> |
|2   <br/> |普通  <br/> |なし  <br/> |**visLORouteStraight** <br/> |
|3   <br/> |組織図  <br/> |上から下へ  <br/> |**visLORouteOrgChartNS** <br/> |
|4   <br/> |組織図  <br/> |左から右へ  <br/> |**visLORouteOrgChartWE** <br/> |
|5   <br/> |フローチャート  <br/> |上から下へ  <br/> |**visLORouteFlowchartNS** <br/> |
|6   <br/> |フローチャート  <br/> |左から右へ  <br/> |**visLORouteFlowchartWE** <br/> |
|7   <br/> |ディレクトリ  <br/> |上から下へ  <br/> |**visLORouteTreeNS** <br/> |
|8   <br/> |ディレクトリ  <br/> |左から右へ  <br/> |**visLORouteTreeWE** <br/> |
|9   <br/> |ネットワーク  <br/> |なし  <br/> |**visLORouteNetwork** <br/> |
|10   <br/> |組織図  <br/> |下から上へ  <br/> |**visLORouteOrgChartSN** <br/> |
|11   <br/> |組織図  <br/> |右から左へ  <br/> |**visLORouteOrgChartEW** <br/> |
|12   <br/> |フローチャート  <br/> |下から上へ  <br/> |**visLORouteFlowchartSN** <br/> |
|13   <br/> |フローチャート  <br/> |右から左へ  <br/> |**visLORouteFlowchartEW** <br/> |
|14   <br/> |ディレクトリ  <br/> |下から上へ  <br/> |**visLORouteTreeSN** <br/> |
|15   <br/> |ディレクトリ  <br/> |右から左へ  <br/> |**visLORouteTreeEW** <br/> |
|16   <br/> |中心から中心へ  <br/> |なし  <br/> |**visloroutecentertocenter** <br/> |
|17   <br/> |単純  <br/> |上から下へ  <br/> |**visLORouteSimpleNS** <br/> |
|18   <br/> |単純  <br/> |左から右へ  <br/> |**visloroutesim*** <br/> |
|年  <br/> |単純  <br/> |下から上へ  <br/> |**visLORouteSimpleSN** <br/> |
|1280  <br/> |単純  <br/> |右から左へ  <br/> |**visloroutesim(新規)** <br/> |
|21  <br/> |シンプル 横 - 縦  <br/> |なし  <br/> |**visloroutesimplehv** <br/> |
|×  <br/> |シンプル 縦 - 横  <br/> |なし  <br/> |**visLORouteSimpleVH** <br/> |
   
## <a name="remarks"></a>注釈

このセルの値は、[**ページ設定**] ダイアログボックスの [**レイアウトと経路**] タブで設定することもできます (このダイアログボックスを開くには、[**デザイン**] タブの [**ページ設定**] 矢印をクリックし、[**レイアウトと経路**] をクリックして、[**間隔**] をクリックします)。 
  
[Shape Layout] セクションの [ShapeRouteStyle] セルでコネクタのローカルな迂回方法を設定できます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [RouteStyle] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |[routestyle]  <br/> |
   
プログラムから、インデックスによって [RouteStyle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLORouteStyle** <br/> |
   

