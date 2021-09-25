---
title: '[ShdwObliqueAngle] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033178
ms.localizationpriority: medium
ms.assetid: 2e0b9754-3e3b-3a26-4e1a-e09102055c20
description: 既定のページの影の種類を適用したときの、斜めの方向を示す数字を指定します。
ms.openlocfilehash: 4982d531663eaf7a854e1a50a50e57b8c52086f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570065"
---
# <a name="shdwobliqueangle-cell-page-properties-section"></a>[ShdwObliqueAngle] セル ([Page Properties] セクション)

既定のページの影の種類を適用したときの、斜めの方向を示す数字を指定します。
  
## <a name="remarks"></a>注釈

このセルの値がゼロ (0) の場合は影の傾きの角度が真上で、時計回りに角度を指定します。
  
 このセルで説明する角度は、ShapeShdwType セル (ページ上の図形の影の種類) が Page Default **(visFSTPageDefault)** に設定され、シャドウの種類が斜めになるたびに使用されます。 既定のページの影の種類は、[Page Properties] セクションの [ShdwType] セルで定義されます。 
  
個々の図形に対してこの動作を設定するには、[Fill Format] セクションで [ShapeShdwObliqueAngle] セルを使用します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwObliqueAngle] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | ShdwObliqueAngle  <br/> |
   
プログラムから、インデックスによって [ShdwObliqueAngle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス :  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPage** <br/> |
| セル インデックス :  <br/> |**visPageShdwObliqueAngle** <br/> |
   

