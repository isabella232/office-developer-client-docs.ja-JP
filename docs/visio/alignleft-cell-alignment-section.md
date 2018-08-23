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
ms.openlocfilehash: f2fc7ef62723812f7dde3f94272a90927272936e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804765"
---
# <a name="alignleft-cell-alignment-section"></a>[AlignLeft] セル ([配置] セクション)

親図形の原点を基準として、図形の左辺を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。
  
## <a name="remarks"></a>備考

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AlignLeft] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [Alignleft]  <br/> |
   
プログラムから、インデックスによって [AlignLeft] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowAlign** <br/> |
| セル インデックス:  <br/> |**visAlignLeft** <br/> |
   

