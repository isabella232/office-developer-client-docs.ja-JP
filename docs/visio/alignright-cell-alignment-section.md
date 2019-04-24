---
title: '[AlignRight] セル ([Alignment] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251297
localization_priority: Normal
ms.assetid: c6d298a4-1602-a53c-bb5d-2ef16b43f722
description: 親図形の原点を基準として、図形の右辺を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。
ms.openlocfilehash: 558808908107a3e42d9d6e4a6fc1cf177150edb9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341504"
---
# <a name="alignright-cell-alignment-section"></a>[AlignRight] セル ([Alignment] セクション)

親図形の原点を基準として、図形の右辺を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。
  
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AlignRight] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [alignright]  <br/> |
   
プログラムから、インデックスによって [AlignRight] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス :  <br/> |**visRowAlign** <br/> |
| セル インデックス:  <br/> |**visAlignRight** <br/> |
   

