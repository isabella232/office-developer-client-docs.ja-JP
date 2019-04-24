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
description: テキスト ブロックの高さを指定します。 既定の数式は次のとおりです。
ms.openlocfilehash: 8ad17cdf1deca6c4aa81f3388d7c112b4e179e2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334392"
---
# <a name="txtheight-cell-text-transform-section"></a>[TxtHeight] セル ([Text Transform] セクション)

テキスト ブロックの高さを指定します。 既定の数式は次のとおりです。
  
= 高さ\* 1
  
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtHeight] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [txtheight]  <br/> |
   
プログラムから、インデックスによって [TxtHeight] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス :  <br/> |**visRowTextXForm** <br/> |
| セル インデックス:  <br/> |**visXFormHeight** <br/> |
   

