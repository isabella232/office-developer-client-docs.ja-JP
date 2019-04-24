---
title: '[ScaleX] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
localization_priority: Normal
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
description: 印刷ページの図面ページの倍率をパーセントで指定します。
ms.openlocfilehash: d1c2f6c184f987e1e7190b1c208310b83a823ee3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326713"
---
# <a name="scalex-cell-print-properties-section"></a>[ScaleX] セル ([Print Properties] セクション)

印刷ページの図面ページの倍率をパーセントで指定します。
  
## <a name="remarks"></a>解説

この値は、OnPage セルの値が FALSE の場合にのみ使用されます。 ScaleX および ScaleY セルの値は常に同じで、[**ページ設定**] ダイアログボックス**** ([**デザイン**] タブの [**ページ設定**] 矢印をクリック) の [**印刷設定**] タブの [設定] に設定されている値に対応しています。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ScaleX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |ScaleX  <br/> |
   
プログラムから、インデックスによって [ScaleX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPrintProperties** <br/> |
|セル インデックス:  <br/> |**visPrintPropertiesScaleX** <br/> |
   

