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
ms.openlocfilehash: b165d43e64842565806d93d620ddbd24f41a2d57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806410"
---
# <a name="shaperoutestyle-cell-shape-layout-section"></a>[ShapeRouteStyle] セル ([Shape Layout] セクション)

図面ページ上にある選択したコネクタの迂回方法と方向を指定します。
  
|**値**|**迂回方法**|**Direction**|**オートメーション定数**|
|:-----|:-----|:-----|:-----|
|0  <br/> |ページの既定値を使用  <br/> |なし  <br/> |**visLORouteDefault** <br/> |
|1  <br/> |直角  <br/> |なし  <br/> |**visLORouteRightAngle** <br/> |
|2  <br/> |直線  <br/> |なし  <br/> |**visLORouteStraight** <br/> |
|3  <br/> |組織図  <br/> |上から下へ  <br/> |**visLORouteOrgChartNS** <br/> |
|4  <br/> |組織図  <br/> |左から右へ  <br/> |**visLORouteOrgChartWE** <br/> |
|5  <br/> |フローチャート  <br/> |上から下へ  <br/> |**visLORouteFlowchartNS** <br/> |
|6  <br/> |フローチャート  <br/> |左から右へ  <br/> |**visLORouteFlowchartWE** <br/> |
|7  <br/> |ツリー状  <br/> |上から下へ  <br/> |**visLORouteTreeNS** <br/> |
|8  <br/> |ツリー状  <br/> |左から右へ  <br/> |**visLORouteTreeWE** <br/> |
|9  <br/> |ネットワーク  <br/> |なし  <br/> |**visLORouteNetwork** <br/> |
|10  <br/> |組織図  <br/> |下から上へ  <br/> |**visLORouteOrgChartSN** <br/> |
|11  <br/> |組織図  <br/> |右から左へ  <br/> |**visLORouteOrgChartEW** <br/> |
|12  <br/> |フローチャート  <br/> |下から上へ  <br/> |**visLORouteFlowchartSN** <br/> |
|13  <br/> |フローチャート  <br/> |右から左へ  <br/> |**visLORouteFlowchartEW** <br/> |
|14  <br/> |ツリー状  <br/> |下から上へ  <br/> |**visLORouteTreeSN** <br/> |
|15  <br/> |ツリー状  <br/> |右から左へ  <br/> |**visLORouteTreeEW** <br/> |
|16  <br/> |中心から中心へ  <br/> |なし  <br/> |**visLORouteCenterToCenter** <br/> |
|17  <br/> |シンプル  <br/> |上から下へ  <br/> |**visLORouteSimpleNS** <br/> |
|18  <br/> |シンプル  <br/> |左から右へ  <br/> |**visLORouteSimpleWE** <br/> |
|19  <br/> |シンプル  <br/> |下から上へ  <br/> |**visLORouteSimpleSN** <br/> |
|20  <br/> |シンプル  <br/> |右から左へ  <br/> |**visLORouteSimpleEW** <br/> |
|21  <br/> |シンプル 横 - 縦  <br/> |なし  <br/> |**visLORouteSimpleHV** <br/> |
|22  <br/> |シンプル 縦 - 横  <br/> |なし  <br/> |**visLORouteSimpleVH** <br/> |
   
## <a name="remarks"></a>備考

**動作**] ダイアログ ボックスで [**コネクタ**] タブで特定のコネクタのこのセルの値を設定することもできます (選択したコネクタで [[開発](run-in-developer-mode-display-the-developer-tab.md)] タブで、[**動作**] をクリックし、 **[コネクタ**] タブをクリックし、)。 
  
ページでこの動作を*すべて*のコネクタを設定するには、[ページ レイアウト] RouteStyle セルを使用します。 
  
Visio 2000 より前のバージョンでは、[Miscellaneous] セクションで [ObjBehavior] セルを使用してこの動作を設定していました。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShapeRouteStyle] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |ShapeRouteStyle  <br/> |
   
プログラムから、インデックスによって [ShapeRouteStyle] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visSLORouteStyle** <br/> |
   

