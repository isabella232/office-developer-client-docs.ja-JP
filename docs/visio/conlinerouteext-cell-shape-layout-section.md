---
title: '[ConLineRouteExt] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50110
ms.localizationpriority: medium
ms.assetid: cafd7589-1c94-b9bc-b1a6-40f7c15fba71
description: コネクタの外観を指定します。
ms.openlocfilehash: f3bba289b4b4f4dc880694b40b8bf835f7cdc321
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577970"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a>[ConLineRouteExt] セル ([Shape Layout] セクション)

コネクタの外観を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 既定値です。ページの設定を使用します。  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | ストレート  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | 曲線  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ConLineRouteExt] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ConLineRouteExt  <br/> |
   
プログラムから、インデックスによって [ConLineRouteExt] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowShapeLayout** <br/> |
| セル インデックス:  <br/> |**visSLOLineRouteExt** <br/> |
   

