---
title: '[AvenueSizeX] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm65
localization_priority: Normal
ms.assetid: 86fe25ed-590d-b2f0-5dfe-9746a19c6b04
description: '[レイアウトの構成] ダイアログボックスを使用して図形をレイアウトするときの、図面ページ上の図形の水平方向の間隔を指定します ([デザイン] タブの [レイアウト] で [ページの再レイアウト] をクリックし、[その他のレイアウトオプション] をクリックします)。'
ms.openlocfilehash: 28eea2589e34c7793e89e01495eb519b987553a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411646"
---
# <a name="avenuesizex-cell-page-layout-section"></a>[AvenueSizeX] セル ([Page Layout] セクション)

[**レイアウトの構成**] ダイアログボックスを使用して図形をレイアウトするときの、図面ページ上の図形の水平方向の間隔を指定します ([**デザイン**] タブの [**レイアウト**] グループで、[**ページの再レイアウト**] をクリックし、[* * More] をクリックします)。レイアウトオプション * *)。
  
## <a name="remarks"></a>注釈

この値は、[**間隔と図形サイズの設定**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブの [**ページ設定**] グループの矢印をクリックし、[**レイアウトと経路**] タブで [**間隔**] をクリックします)。
  
ダイナミック グリッドでは、左右間隔の計算対象となる図形が 1 つだけある場合に [AvenueSizeX] セルの設定が使用されます。ダイナミック グリッドを使用するには、[**表示**] タブの [**視覚的補助**] グループで、[**ダイナミック グリッド**] チェック ボックスをオンにします。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AvenueSizeX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [avenuesizey]  <br/> |
   
プログラムから、インデックスによって [AvenueSizeX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visPLOAvenueSizeX** <br/> |
   

