---
title: '[ShdwObliqueAngle] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033178
localization_priority: Normal
ms.assetid: 2e0b9754-3e3b-3a26-4e1a-e09102055c20
description: 既定のページの影の種類を適用したときの、斜めの方向を示す数字を指定します。
ms.openlocfilehash: 4549ce7b5202b4649a925b04ea54c0d5df569599
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806474"
---
# <a name="shdwobliqueangle-cell-page-properties-section"></a>[ShdwObliqueAngle] セル ([ページのプロパティ] セクション)

既定のページの影の種類を適用したときの、斜めの方向を示す数字を指定します。
  
## <a name="remarks"></a>備考

このセルの値がゼロ (0) の場合は影の傾きの角度が真上で、時計回りに角度を指定します。
  
 ShapeShdwType セル (ページ上の図形の影の種類) がページの既定値 (**visFSTPageDefault** ) に設定し、影の種類は、斜体にするたびに、このセルに記載されている角度が使用されます。 既定ページの影の種類は、[shdwtype] セルで定義されます。 
  
個々の図形に対してこの動作を設定するには、[Fill Format] セクションで [ShapeShdwObliqueAngle] セルを使用します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwObliqueAngle] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | ShdwObliqueAngle  <br/> |
   
プログラムから、インデックスによって [ShdwObliqueAngle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPage** <br/> |
| セル インデックス:  <br/> |**visPageShdwObliqueAngle** <br/> |
   

