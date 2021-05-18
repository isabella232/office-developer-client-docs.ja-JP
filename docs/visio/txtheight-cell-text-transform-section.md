---
title: '[TxtHeight] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1025
localization_priority: Normal
ms.assetid: cfa3ecc6-61a8-506c-ba1d-b5e1f757d44f
description: テキスト ブロックの高さを指定します。既定の数式は次のとおりです。
ms.openlocfilehash: 8ad17cdf1deca6c4aa81f3388d7c112b4e179e2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409308"
---
# <a name="txtheight-cell-text-transform-section"></a>[TxtHeight] セル ([Text Transform] セクション)

テキスト ブロックの高さを指定します。既定の数式は次のとおりです。
  
= 高 \* さ 1
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtHeight] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | TxtHeight  <br/> |
   
プログラムから、インデックスによって [TxtHeight] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス :  <br/> |**visRowTextXForm** <br/> |
| セル インデックス:  <br/> |**visXFormHeight** <br/> |
   

