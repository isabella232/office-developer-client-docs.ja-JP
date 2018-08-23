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
description: レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときは、図面ページ上の図形間の垂直方向のスペースの量を決定する ([デザイン] タブの [レイアウト] で、再レイアウト] ページをクリックし、他のレイアウト オプションをクリックし、)。
ms.openlocfilehash: af4089a3b215efaf49b8a45929ca94799fffcba5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804799"
---
# <a name="avenuesizey-cell-page-layout-section"></a>[AvenueSizeY] セル ([ページ レイアウト] セクション)

**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトするときは、図面ページ上の図形間の垂直方向のスペースの量を決定する ([**デザイン**] タブの [**レイアウト**] で、ページの**再レイアウト**] をクリックし、**よりレイアウト オプション**)。
  
## <a name="remarks"></a>注釈

この値は、[**間隔と図形サイズの設定**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブの [**ページ設定**] グループの矢印をクリックし、[**レイアウトと経路**] タブをクリックして、[**間隔**] をクリックします)。
  
ダイナミック グリッドでは、上下の間隔の計算対象となる図形が 1 つだけある場合に [AvenueSizeY] セルの設定が使用されます。ダイナミック グリッドを使用するには、[**表示**] タブの [**視覚的補助**] グループで、[**ダイナミック グリッド**] チェック ボックスをオンにします。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AvenueSizeY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [Avenuesizey]  <br/> |
   
プログラムから、インデックスによって [AvenueSizeY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visPLOAvenueSizeY** <br/> |
   

