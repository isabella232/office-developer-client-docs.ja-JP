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
ms.openlocfilehash: d64e7b3c7cf30f0a657ede57b227acefd4b10101
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806272"
---
# <a name="routestyle-cell-page-layout-section"></a>[RouteStyle] セル ([Page Layout] セクション)

ローカルな迂回方法を持たない図面ページ上のすべてのコネクタに対して、迂回方法と方向を指定します。
  
|**値**|**迂回方法**|**Direction**|**オートメーション定数**|
|:-----|:-----|:-----|:-----|
|0  <br/> |直角 (既定値)  <br/> |なし  <br/> |**visLORouteDefault** <br/> |
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

**[ページ設定**] ダイアログ ボックスで、[**レイアウトと経路**] タブで、このセルの値を設定することもできます ([**デザイン**] タブで、 **[ページ設定**の矢印をクリックして、[**レイアウトと経路**、および、[**間隔**] をクリック) します。 
  
[Shape Layout] セクションの [ShapeRouteStyle] セルでコネクタのローカルな迂回方法を設定できます。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[RouteStyle] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |RouteStyle  <br/> |
   
プログラムから、インデックスによって [RouteStyle] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLORouteStyle** <br/> |
   

