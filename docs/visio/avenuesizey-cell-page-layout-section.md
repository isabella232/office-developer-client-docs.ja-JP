---
title: '[AvenueSizeY] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm70
localization_priority: Normal
ms.assetid: 9ff2893c-afe5-505e-0b55-48ec1de08a5f
description: '[レイアウトの構成] ダイアログボックスを使用して図形をレイアウトするときの、図面ページ上の図形の垂直方向の間隔を指定します ([デザイン] タブの [レイアウト] で [ページの再レイアウト] をクリックし、[その他のレイアウトオプション] をクリックします)。'
ms.openlocfilehash: 283de8925e34c470fd1f9e78b8ae58882be8b7fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338424"
---
# <a name="avenuesizey-cell-page-layout-section"></a>[AvenueSizeY] セル ([Page Layout] セクション)

[**レイアウトの構成**] ダイアログボックスを使用して図形をレイアウトするときの、図面ページ上の図形の垂直方向の間隔を指定します ([**デザイン**] タブの [**レイアウト**] で [ページの**再レイアウト**] をクリックし、[その他] をクリックします)。 **レイアウトオプション**)。
  
## <a name="remarks"></a>解説

この値は、[**間隔と図形サイズの設定**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブの [**ページ設定**] グループの矢印をクリックし、[**レイアウトと経路**] タブをクリックして、[**間隔**] をクリックします)。
  
ダイナミック グリッドでは、上下の間隔の計算対象となる図形が 1 つだけある場合に [AvenueSizeY] セルの設定が使用されます。ダイナミック グリッドを使用するには、[**表示**] タブの [**視覚的補助**] グループで、[**ダイナミック グリッド**] チェック ボックスをオンにします。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AvenueSizeY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [avenuesizey]  <br/> |
   
プログラムから、インデックスによって [AvenueSizeY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visPLOAvenueSizeY** <br/> |
   

