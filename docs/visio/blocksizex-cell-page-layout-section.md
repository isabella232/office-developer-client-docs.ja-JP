---
title: '[BlockSizeX] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm105
localization_priority: Normal
ms.assetid: 253aac17-077e-48e0-39a8-a3abd5d4a257
description: '[レイアウトの構成] ダイアログボックス ([デザイン] タブの [レイアウト] で [ページの再レイアウト] をクリックし、[その他のレイアウトオプション] をクリック) を使用して図形をレイアウトするときに、水平方向のブロックサイズを決定します。'
ms.openlocfilehash: 8e4cee4b2059d9b8f2fe77c2d4902e67246eac2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309479"
---
# <a name="blocksizex-cell-page-layout-section"></a>[BlockSizeX] セル ([Page Layout] セクション)

[**レイアウトの構成**] ダイアログボックスを使用して図形をレイアウトするときに、図形の各図形が図面ページ上に配置される領域 ([**デザイン**] タブの [**レイアウト**] グループで、[**ページの再レイアウト] をクリックします) を指定します。** をクリックし、[その**他のレイアウトオプション**] をクリックします)。
  
## <a name="remarks"></a>解説

この値は、[**間隔と図形サイズの設定**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブの [**ページ設定**] グループの矢印をクリックし、[**レイアウトと経路**] タブをクリックして、[**間隔**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BlockSizeX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[blocksizex]  <br/> |
   
プログラムから、インデックスによって [BlockSizeX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visploblocksizex** <br/> |
   

