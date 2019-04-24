---
title: '[AlignBottom] セル ([Alignment] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm20
localization_priority: Normal
ms.assetid: 234e7ffa-04e3-0204-c5be-7ff7a4d0d54c
description: 親図形の原点を基準として、図形の下部の辺を揃えるための水平ガイドまたはガイド点の垂直方向の位置を指定します。
ms.openlocfilehash: 66fea9949f2f31eb5c3aaf43804ac0ec9f7e20fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346565"
---
# <a name="alignbottom-cell-alignment-section"></a>[AlignBottom] セル ([Alignment] セクション)

親図形の原点を基準として、図形の下部の辺を揃えるための水平ガイドまたはガイド点の垂直方向の位置を指定します。
  
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AlignBottom] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | alignbottom]  <br/> |
   
プログラムから、インデックスによって [AlignBottom] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス :  <br/> |**visRowAlign** <br/> |
| セル インデックス:  <br/> |**visAlignBottom** <br/> |
   

