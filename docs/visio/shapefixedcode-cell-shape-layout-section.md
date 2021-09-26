---
title: '[ShapeFixedCode] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm880
ms.localizationpriority: medium
ms.assetid: a1736a5c-421c-2bdb-b164-76a8cd06cc3d
description: 配置可能な図形について、配置時の動作を指定します。
ms.openlocfilehash: 71dcee0cd60f702c138389c437c6dc4eb4895eb2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627479"
---
# <a name="shapefixedcode-cell-shape-layout-section"></a>[ShapeFixedCode] セル ([Shape Layout] セクション)

配置可能な図形について、配置時の動作を指定します。
  
|**値**|**選択モード**|**オートメーション定数**|
|:-----|:-----|:-----|
|&amp;H1  <br/> |[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに、この **図形を** 移動しない。  <br/> |**visSLOFixedPlacement** <br/> |
|&amp;H2  <br/> |この図形は移動しません。また他の図形をこの図形の上に配置できません。  <br/> |**visSLOFixedPlow** <br/> |
|&amp;H4  <br/> |この図形は移動しません。ただし他の図形をこの図形の上に配置できます。  <br/> |**visSLOFixedPermeablePlow** <br/> |
|&amp;H20 (32)  <br/> |迂回するときに、接続ポイントの位置を無視します。  <br/> |**visSLOFixedConnPtsIgnore** <br/> |
|&amp;H40 (64)  <br/> |接続ポイントがある側だけに迂回します。  <br/> |**visSLOFixedConnPtsOnly** <br/> |
|&amp;H80 (128)  <br/> |この図形の外周には接着しません。代わりに、図形の図形枠に接着します。  <br/> |**visSLOFixedNoFoldToShape** <br/> |
   
## <a name="remarks"></a>注釈

[動作] ダイアログ ボックスの [配置] タブで、このセルの値を設定することもできます (図形が選択されている場合は、[開発] タブの[図形のデザイン] グループで、[動作] をクリックし、[配置] タブ **をクリック** します)。  [](run-in-developer-mode-display-the-developer-tab.md) 
  
このセルには、上記の値を任意に組み合わせて設定できます。 たとえば、値 3 ( H3) を入力すると、[レイアウトの構成] ダイアログ ボックス &amp; ([デザイン] タブの [レイアウト]グループで、[レイアウトの再レイアウト] ページ) をクリックし、[その他のレイアウト オプション] をクリックして、図形の上または近くに他の配置可能な図形を配置すると、図形をレイアウトするときに移動を排除できます。 
  
Visio 2000 より前のバージョンでは、[Miscellaneous] セクションで [ObjInteract] セルを使用してこの動作を設定していました。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapeFixedCode] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |ShapeFixedCode  <br/> |
   
プログラムから、インデックスによって [ShapeFixedCode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visSLOFixedCode** <br/> |
   

