---
title: '[AlignLeft] セル ([Alignment] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm30
localization_priority: Normal
ms.assetid: d094411e-ed65-1d0d-5c35-68b003da2696
description: 親図形の原点を基準として、図形の左辺を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。
ms.openlocfilehash: 5fdf1251c8829fd644d1a4bfd5eab8890c0d3e71
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346544"
---
# <a name="alignleft-cell-alignment-section"></a>[AlignLeft] セル ([Alignment] セクション)

親図形の原点を基準として、図形の左辺を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。
  
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AlignLeft] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [alignleft]  <br/> |
   
プログラムから、インデックスによって [AlignLeft] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス :  <br/> |**visRowAlign** <br/> |
| セル インデックス:  <br/> |**visAlignLeft** <br/> |
   

