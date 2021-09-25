---
title: '[ScaleX] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
ms.localizationpriority: medium
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
description: プリンター ページの図面ページの倍率の割合を指定します。
ms.openlocfilehash: 457aec2fdb00c082e9689f9b0a98e5104af39893
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573433"
---
# <a name="scalex-cell-print-properties-section"></a>[ScaleX] セル ([Print Properties] セクション)

プリンター ページの図面ページの倍率の割合を指定します。
  
## <a name="remarks"></a>注釈

この値は、OnPage セルの値が FALSE の場合にのみ使用されます。 ScaleX セルと ScaleY セルの値は常に同じです。これは、[ページセットアップ] ダイアログボックスの [印刷設定] タブの [調整] 設定の値に対応します ([デザイン] タブの [ページ設定] 矢印を **クリック** します)。  
  
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
   

