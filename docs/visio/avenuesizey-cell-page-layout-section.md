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
# <a name="avenuesizey-cell-page-layout-section"></a>[AvenueSizeY] セル ([Page Layout] セクション)

**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトするときは、図面ページ上の図形間の垂直方向のスペースの量を決定する ([**デザイン**] タブの [**レイアウト**] で、ページの**再レイアウト**] をクリックし、**よりレイアウト オプション**)。
  
## <a name="remarks"></a>備考

**レイアウトと間隔**] ダイアログ ボックスでこの値を設定することもできます ([**デザイン**] タブで、[**ページ設定**] で矢印をクリックして、**レイアウトと経路**] タブをクリックし、[**間隔**] をクリック) します。
  
ダイナミック グリッドでは、のみ 1 つの図形は垂直方向の間隔を計算するために利用可能な場合に [avenuesizey] セルで設定を使用します。 [**表示**] タブの [**視覚補助**] では、ダイナミック グリッドを使用するには、**ダイナミック グリッド**を選択します。
  
取得する [avenuesizey] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [Avenuesizey]  <br/> |
   
プログラムから、インデックスによって [avenuesizey] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visPLOAvenueSizeY** <br/> |
   

