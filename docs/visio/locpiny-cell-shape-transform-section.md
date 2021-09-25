---
title: '[LocPinY] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm685
ms.localizationpriority: medium
ms.assetid: a29c5d4e-d3d6-d984-495a-4b0b130352ef
description: 図形の原点に対する図形のピン (回転の中心) の y 座標を表します。 [LocPinY] を決定する既定の数式は次のとおりです。
ms.openlocfilehash: 3e9ff2fd0daf3f75e1e1b341a37836e0ccc70831
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623363"
---
# <a name="locpiny-cell-shape-transform-section"></a>[LocPinY] セル ([Shape Transform] セクション)

図形の原点に対する図形のピン (回転の中心) の  *y*  座標を表します。 [LocPinY] を決定する既定の数式は次のとおりです。 
  
= 高 \* さ 0.5
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LocPinY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LocPinY  <br/> |
   
プログラムから、インデックスによって [LocPinY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowXFormOut** <br/> |
| セル インデックス:  <br/> |**visXFormLocPinY** <br/> |
   

