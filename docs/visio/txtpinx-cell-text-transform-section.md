---
title: '[TxtPinX] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
ms.localizationpriority: medium
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: 図形の原点に対するテキスト ブロックの回転中心の x 座標を指定します。 既定の数式は次のとおりです。
ms.openlocfilehash: 7cd62258558fc9657a62b1e3e39811acac973527
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569854"
---
# <a name="txtpinx-cell-text-transform-section"></a>[TxtPinX] セル ([Text Transform] セクション)

図形の  *原点に*  対するテキスト ブロックの回転中心の x 座標を指定します。 既定の数式は次のとおりです。 
  
= 幅 \* 0.5
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtPinX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | TxtPinX  <br/> |
   
プログラムから、インデックスによって [TxtPinX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス :  <br/> |**visRowTextXForm** <br/> |
| セル インデックス:  <br/> |**visXFormPinX** <br/> |
   

