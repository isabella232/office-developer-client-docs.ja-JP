---
title: '[PrintGrid] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033794
localization_priority: Normal
ms.assetid: 0504ff7f-2274-7ae3-1f4b-a3d890dbd79a
description: 図面ページの印刷時にグリッドを印刷するかどうかを指定します。
ms.openlocfilehash: 76e5b5b4e82c39cbbffbecc710f05a77dbaa6332
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806125"
---
# <a name="printgrid-cell-print-properties-section"></a>[PrintGrid] セル ([Print Properties] セクション)

図面ページの印刷時にグリッドを印刷するかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |このページの印刷時にグリッドを表示します。  <br/> |
|FALSE  <br/> |このページの印刷時にグリッドを表示しません (既定値)。  <br/> |
   
## <a name="remarks"></a>注釈

この値は、[**ページ設定**] ダイアログ ボックスの [**印刷設定**] タブで [**目盛線**] チェック ボックスに対応 ([**デザイン**] タブで、矢印をクリック、 **[ページ設定**)。 以外の色 (印刷用グレー)、印刷されたグリッドは、Microsoft Visio の図面ウィンドウに表示するグリッドと同じです。 
  
ページごとにグリッドを印刷するかどうかを選択することができます。 ページごとにグリッドのスタイルを定義することも、**ルーラー&amp;グリッド**] ダイアログ ボックス ([**表示**] タブで、矢印をクリック**を表示する**)、ページがアクティブな場合。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [printgrid] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[Printgrid]  <br/> |
   
プログラムから、インデックスによって [printgrid] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPrintProperties** <br/> |
|セル インデックス:  <br/> |**visPrintPropertiesPrintGrid** <br/> |
   
