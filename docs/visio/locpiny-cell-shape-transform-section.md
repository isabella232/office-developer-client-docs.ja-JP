---
title: '[LocPinY] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm685
localization_priority: Normal
ms.assetid: a29c5d4e-d3d6-d984-495a-4b0b130352ef
description: Y を表す-図形の原点を基準として、図形の pin (回転の中心) の座標。 [Locpiny] を決定するための既定の数式は次のとおりです。
ms.openlocfilehash: 8d98906e8082af0fc54bc01fe3a8537b66ac56b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805789"
---
# <a name="locpiny-cell-shape-transform-section"></a>[LocPinY] セル ([図形変換] セクション)

*Y*を表す-図形の原点を基準として、図形の pin (回転の中心) の座標。 [Locpiny] を決定するための既定の数式は次のとおりです。 
  
= 高さ\*0.5
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LocPinY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [Locpiny]  <br/> |
   
プログラムから、インデックスによって [LocPinY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowXFormOut** <br/> |
| セル インデックス:  <br/> |**visXFormLocPinY** <br/> |
   

