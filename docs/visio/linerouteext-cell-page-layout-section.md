---
title: '[LineRouteExt] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50115
ms.localizationpriority: medium
ms.assetid: 3d16b8b3-601b-c10b-68a8-ffd47251306f
description: 図面ページにあるすべてのコネクタの既定の外観を指定します。
ms.openlocfilehash: 37bcf569b4a095ed1b3e08823db1673ef5cc95cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615887"
---
# <a name="linerouteext-cell-page-layout-section"></a>[LineRouteExt] セル ([Page Layout] セクション)

図面ページにあるすべてのコネクタの既定の外観を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 既定値 (直線)  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | ストレート  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | 曲線  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineRouteExt] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LineRouteExt  <br/> |
   
プログラムから、インデックスによって [LineRouteExt] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visPLOLineRouteExt** <br/> |
   

