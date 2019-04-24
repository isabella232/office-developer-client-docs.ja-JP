---
title: '[xrulerorigin] セル&amp; ([ルーラ Grid] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1170
localization_priority: Normal
ms.assetid: 328f8ab5-217f-0336-0d56-611eff509fe8
description: ページの x 軸のルーラーに対して、ゼロ点を指定します。
ms.openlocfilehash: d66fd324718ec46b1209c4726eeb2d27c21db8b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346453"
---
# <a name="xrulerorigin-cell-ruler-amp-grid-section"></a>[xrulerorigin] セル&amp; ([ルーラ Grid] セクション)

ページの x 軸のルーラーに対して、ゼロ点を指定します。
  
## <a name="remarks"></a>解説

このセルは、[**ルーラー &amp;グリッド**] ダイアログボックス ([**表示**] タブの [**表示**] 矢印をクリック) の [水平**ルーラーゼロ**] オプションに対応しています。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [XRulerOrigin] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |[xrulerorigin]  <br/> |
   
プログラムから、インデックスによって [XRulerOrigin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowRulerGrid** <br/> |
|セル インデックス:  <br/> |**visXRulerOrigin** <br/> |
   

