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
description: X を表す-図形の原点を基準として、図形の pin (回転の中心) の座標。 [Locpinx] を決定するための既定の数式は次のとおりです。
ms.openlocfilehash: 17f7b0fde9a54f6596f2f87f866d30b908e062b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805802"
---
# <a name="locpinx-cell-shape-transform-section"></a>[LocPinX] セル ([図形変換] セクション)

*X*を表す-図形の原点を基準として、図形の pin (回転の中心) の座標。 [Locpinx] を決定するための既定の数式は次のとおりです。 
  
= 幅\*0.5
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LocPinX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [Locpinx]  <br/> |
   
プログラムから、インデックスによって [LocPinX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowXFormOut** <br/> |
| セル インデックス:  <br/> |**visXFormLocPinX** <br/> |
   

