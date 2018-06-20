---
title: '[PageScale] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm775
localization_priority: Normal
ms.assetid: e1da84b3-fd15-12b9-9342-0412e818b3b9
description: 現在の図面縮尺でページ単位の値を指定します。ページの図面縮尺は、[DrawingScale] セルに表示される図面単位に対して [PageScale] セルに表示されるページ単位の比率です。
ms.openlocfilehash: 0e1721ea667ad3bcd9f35880ab4e63bc90802c32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806001"
---
# <a name="pagescale-cell-page-properties-section"></a>[PageScale] セル ([Page Properties] セクション)

現在の図面縮尺でページ単位の値を指定します。ページの図面縮尺は、[DrawingScale] セルに表示される図面単位に対して [PageScale] セルに表示されるページ単位の比率です。
  
## <a name="remarks"></a>注釈

**[ページ設定**] ダイアログ ボックスで [**図面縮尺**] タブの [pagescale] セルの値を設定することもできます ([**デザイン**] タブで、矢印をクリック、 **[ページ設定**)。 セルの値は、最初の**既定の縮尺**] ボックスまたは **[縮尺**] ボックスの [**図面縮尺**で選択した図面縮尺の設定に応じて、2 つの数値です。 などの場合は、図面に建築系縮尺を選択すると、ページの図面縮尺は 3/32"= 1'0"です。 [Pagescale] セルの値は 0.0938 のです。 (または 3/32 インチ) し、[DrawingScale] セルに値が 1 フィートです。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [pagescale] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[Pagescale]  <br/> |
   
プログラムから、インデックスによって [pagescale] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPage** <br/> |
|セル インデックス:  <br/> |**visPageScale** <br/> |
   

