---
title: '[ConLineRouteExt] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50110
localization_priority: Normal
ms.assetid: cafd7589-1c94-b9bc-b1a6-40f7c15fba71
description: コネクタの外観を指定します。
ms.openlocfilehash: 19fe948daf7aa3d67db858849ecb2b15f40ba02d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434614"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a>[ConLineRouteExt] セル ([Shape Layout] セクション)

コネクタの外観を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| .0  <br/> | 既定値です。ページの設定を使用します。  <br/> |**visLORouteExtDefault** <br/> |
| 1   <br/> | 普通  <br/> |**visLORouteExtStraight** <br/> |
| 2   <br/> | 曲線  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ConLineRouteExt] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [conlinerouteext]  <br/> |
   
プログラムから、インデックスによって [ConLineRouteExt] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowShapeLayout** <br/> |
| セル インデックス:  <br/> |**visSLOLineRouteExt** <br/> |
   

