---
title: '[ShapeFixedCode] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm880
localization_priority: Normal
ms.assetid: a1736a5c-421c-2bdb-b164-76a8cd06cc3d
description: 配置可能な図形について、配置時の動作を指定します。
ms.openlocfilehash: 6ae83fa70cc545c88080ce27046bd8c226c060e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806386"
---
# <a name="shapefixedcode-cell-shape-layout-section"></a>[ShapeFixedCode] セル ([図形レイアウト] セクション)

配置可能な図形について、配置時の動作を指定します。
  
|**値**|**選択モード**|**オートメーション定数**|
|:-----|:-----|:-----|
|&amp;H1  <br/> |**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトするとき、この図形を移動しません。  <br/> |**visSLOFixedPlacement** <br/> |
|&amp;H2  <br/> |この図形は移動しません。また他の図形をこの図形の上に配置できません。  <br/> |**visSLOFixedPlow** <br/> |
|&amp;H4  <br/> |この図形は移動しません。ただし他の図形をこの図形の上に配置できます。  <br/> |**visSLOFixedPermeablePlow** <br/> |
|&amp;H20 (32)  <br/> |迂回するときに、接続ポイントの位置を無視します。  <br/> |**visSLOFixedConnPtsIgnore** <br/> |
|&amp;H40 (64)  <br/> |接続ポイントがある側だけに迂回します。  <br/> |**visSLOFixedConnPtsOnly** <br/> |
|&amp;H80 (128)  <br/> |この図形の外周には接着しません。代わりに、図形の図形枠に接着します。  <br/> |**visSLOFixedNoFoldToShape** <br/> |
   
## <a name="remarks"></a>注釈

**動作**] ダイアログ ボックスの [**配置**] タブで、このセルの値を設定することもできます (図形を選択して、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] で、[**動作**] をクリックし、[**配置**] タブをクリックして). 
  
このセルの値の任意の組み合わせを設定することができます。 値 3 を入力するたとえば、(&amp;H3)、**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトするときの動きを排除する ([**デザイン**] タブの [**レイアウト**] で、**ページの再レイアウト**] をクリックし、 **他のレイアウト オプション**) または図形の近くに他の配置可能な図形を配置するときとします。 
  
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
   

