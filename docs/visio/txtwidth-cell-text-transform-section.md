---
title: '[TxtWidth] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251270
localization_priority: Normal
ms.assetid: e2215c67-25fa-1d75-9cce-f126bb8760a1
description: テキスト ブロックの幅を指定します。既定の数式は次のとおりです。
ms.openlocfilehash: 806307166035ebc2f8e20e7025d5ecb03c4d6e79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426094"
---
# <a name="txtwidth-cell-text-transform-section"></a>[TxtWidth] セル ([Text Transform] セクション)

テキスト ブロックの幅を指定します。既定の数式は次のとおりです。
  
= 幅 \* 1
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtWidth] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | TxtWidth  <br/> |
   
プログラムから、インデックスによって [TxtWidth] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス :  <br/> |**visRowTextXForm** <br/> |
| セル インデックス:  <br/> |**visXFormWidth** <br/> |
   

