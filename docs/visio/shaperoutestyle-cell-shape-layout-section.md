---
title: '[ShapeRouteStyle] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm905
localization_priority: Normal
ms.assetid: a5dcd2e0-e343-5ee2-2b63-2a1312437901
description: 図面ページ上にある選択したコネクタの迂回方法と方向を指定します。
ms.openlocfilehash: e5725d461a71dad4623161d99134a20250abe724
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425030"
---
# <a name="shaperoutestyle-cell-shape-layout-section"></a>[ShapeRouteStyle] セル ([Shape Layout] セクション)

図面ページ上にある選択したコネクタの迂回方法と方向を指定します。
  
|**値**|**迂回方法**|**Direction**|**オートメーション定数**|
|:-----|:-----|:-----|:-----|
|.0  <br/> |ページの既定値を使用  <br/> |なし  <br/> |**visLORouteDefault** <br/> |
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

このセルの値は、[**基本動作**] ダイアログボックスの [**コネクタ**] タブで、コネクタが選択されている状態で、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**基本動作**] をクリックし、[**コネクタ**] タブをクリックして、特定のコネクタに対して設定することもできます。 
  
ページ上の*すべて*のコネクタに対してこの動作を設定するには、[ページレイアウト] セクションの [routestyle] セルを使用します。 
  
Visio 2000 より前のバージョンでは、[Miscellaneous] セクションで [ObjBehavior] セルを使用してこの動作を設定していました。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapeRouteStyle] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |[shaperoutestyle]  <br/> |
   
プログラムから、インデックスによって [ShapeRouteStyle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visSLORouteStyle** <br/> |
   

