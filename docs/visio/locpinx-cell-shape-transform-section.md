---
title: '[LocPinX] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm680
localization_priority: Normal
ms.assetid: b82feade-5793-8a6e-3ff4-69a4cbdd2cf9
description: 図形の原点を基準としたときの、図形の pin (回転の中心) の x 座標を表します。 [LocPinX] を決定する既定の数式は次のとおりです。
ms.openlocfilehash: 2eb5c328eed3c97652173670c426b83b8c358833
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439241"
---
# <a name="locpinx-cell-shape-transform-section"></a>[LocPinX] セル ([Shape Transform] セクション)

図形の原点を基準としたときの、図形の pin (回転の中心) の*x*座標を表します。 [LocPinX] を決定する既定の数式は次のとおりです。 
  
= 幅\* 0.5
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LocPinX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [locpinx]  <br/> |
   
プログラムから、インデックスによって [LocPinX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowXFormOut** <br/> |
| セル インデックス:  <br/> |**visXFormLocPinX** <br/> |
   

