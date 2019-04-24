---
title: '[ScaleY] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
localization_priority: Normal
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
description: 印刷ページの図面ページの倍率をパーセントで指定します。
ms.openlocfilehash: 0f8e86675a039002b60438eac7df92f4a2b13b98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342729"
---
# <a name="scaley-cell-print-properties-section"></a>[ScaleY] セル ([Print Properties] セクション)

印刷ページの図面ページの倍率をパーセントで指定します。
  
## <a name="remarks"></a>解説

この値は、OnPage セルの値が FALSE の場合にのみ使用されます。 ScaleX および ScaleY セルの値は常に同じで、[**ページ設定**] ダイアログボックス**** ([**デザイン**] タブの [**ページ設定**] 矢印をクリック) の [**印刷設定**] タブの [設定] に設定されている値に対応しています。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ScaleY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |ScaleY  <br/> |
   
プログラムから、インデックスによって [ScaleY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPrintProperties** <br/> |
|セル インデックス:  <br/> |**visPrintPropertiesScaleY** <br/> |
   

