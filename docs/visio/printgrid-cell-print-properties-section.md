---
title: '[PrintGrid] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033794
ms.localizationpriority: medium
ms.assetid: 0504ff7f-2274-7ae3-1f4b-a3d890dbd79a
description: 図面ページの印刷時にグリッドを印刷するかどうかを指定します。
ms.openlocfilehash: e290e28920f3ece4f9493b52b223e85dc3888949
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559760"
---
# <a name="printgrid-cell-print-properties-section"></a>[PrintGrid] セル ([Print Properties] セクション)

図面ページの印刷時にグリッドを印刷するかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |このページの印刷時にグリッドを表示します。  <br/> |
|FALSE  <br/> |このページの印刷時にグリッドを表示しません (既定値)。  <br/> |
   
## <a name="remarks"></a>注釈

この値は、[**ページ設定**] ダイアログ ボックスの [**プリンターの設定**] タブにある [**目盛線**] チェック ボックスに対応しています (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックします)。印刷されたグリッドは、色 (印刷ではグレー) 以外の点では、Microsoft Visio 図面ウィンドウに表示されるグリッドと同じです。 
  
グリッドを 1 ページずつ印刷するかどうかを選択できます。 グリッドのスタイルは、ページがアクティブなときに **[Ruler &amp; Grid]** ダイアログ ボックス ([表示]タブの [表示] 矢印をクリック) でページ単位で定義することもできます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PrintGrid] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |PrintGrid  <br/> |
   
プログラムから、インデックスによって [PrintGrid] セルへの参照を取得するには、**CellsSRC** プロパティを使用します。次の引数を指定してください。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPrintProperties** <br/> |
|セル インデックス:  <br/> |**visPrintPropertiesPrintGrid** <br/> |
   

