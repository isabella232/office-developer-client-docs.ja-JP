---
title: '[LineRouteExt] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50115
localization_priority: Normal
ms.assetid: 3d16b8b3-601b-c10b-68a8-ffd47251306f
description: 図面ページにあるすべてのコネクタの既定の外観を指定します。
ms.openlocfilehash: 21da283f2d9ab43837b8fe4127840e89ea9d9949
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805724"
---
# <a name="linerouteext-cell-page-layout-section"></a>[LineRouteExt] セル ([Page Layout] セクション)

図面ページにあるすべてのコネクタの既定の外観を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 既定値 (直線)  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | 直線  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | 曲線  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LineRouteExt] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LineRouteExt  <br/> |
   
プログラムから、インデックスによって [LineRouteExt] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visPLOLineRouteExt** <br/> |
   

