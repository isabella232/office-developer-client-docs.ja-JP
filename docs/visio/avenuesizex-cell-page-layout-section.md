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
description: レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときは、図面ページ上の図形間の水平方向のスペースの量を決定する ([デザイン] タブの [レイアウト] で、再レイアウト] ページをクリックし、他のレイアウト オプションをクリックし、)。
ms.openlocfilehash: efb29181414957063e038b97c2d7b79720aa0405
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804806"
---
# <a name="avenuesizex-cell-page-layout-section"></a>[AvenueSizeX] セル ([Page Layout] セクション)

**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトするときは、図面ページ上の図形間の水平方向のスペースの量を決定する ([**デザイン**] タブの [**レイアウト**] で、 **[再レイアウト] ページ**をクリック * * よりレイアウト オプション * *)。
  
## <a name="remarks"></a>備考

**レイアウトと間隔**] ダイアログ ボックスでこの値を設定することもできます ([**デザイン**] タブで、[**ページ設定**] で矢印をクリックして、**レイアウトと経路**] タブをクリックし、[**間隔**] をクリック) します。
  
ダイナミック グリッドは、1 つだけ図形が水平方向の間隔を計算するために利用可能な [avenuesizex] セルの設定を使用します。 [**表示**] タブの [**視覚補助**] では、ダイナミック グリッドを使用するには、**ダイナミック グリッド**を選択します。
  
取得する [avenuesizex] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [Avenuesizey]  <br/> |
   
プログラムから、インデックスによって [avenuesizex] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visPLOAvenueSizeX** <br/> |
   

