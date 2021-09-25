---
title: '[ScaleY] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
ms.localizationpriority: medium
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
description: プリンター ページの図面ページの倍率の割合を指定します。
ms.openlocfilehash: d4a84ef5a7d9d158ec64bab61cc18ffa6c794b97
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573426"
---
# <a name="scaley-cell-print-properties-section"></a>[ScaleY] セル ([Print Properties] セクション)

プリンター ページの図面ページの倍率の割合を指定します。
  
## <a name="remarks"></a>注釈

この値は、OnPage セルの値が FALSE の場合にのみ使用されます。 ScaleX セルと ScaleY セルの値は常に同じです。これは、[ページセットアップ] ダイアログボックスの [印刷設定] タブの [調整] 設定の値に対応します ([デザイン] タブの [ページ設定] 矢印を **クリック** します)。  
  
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
   

