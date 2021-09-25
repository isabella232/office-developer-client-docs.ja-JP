---
title: '[LocPinX] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm680
ms.localizationpriority: medium
ms.assetid: b82feade-5793-8a6e-3ff4-69a4cbdd2cf9
description: 図形の原点に対する図形のピン (回転の中心) の x 座標を表します。 [LocPinX] を決定する既定の数式は次のとおりです。
ms.openlocfilehash: 0ff3815f474ce9ffaec543855092c197aa51a6a9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582513"
---
# <a name="locpinx-cell-shape-transform-section"></a>[LocPinX] セル ([Shape Transform] セクション)

図形の  *原点に*  対する図形のピン (回転の中心) の x 座標を表します。 [LocPinX] を決定する既定の数式は次のとおりです。 
  
= 幅 \* 0.5
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LocPinX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LocPinX  <br/> |
   
プログラムから、インデックスによって [LocPinX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowXFormOut** <br/> |
| セル インデックス:  <br/> |**visXFormLocPinX** <br/> |
   

