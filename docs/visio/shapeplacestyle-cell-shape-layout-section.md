---
title: '[ShapePlaceStyle] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm70007
ms.localizationpriority: medium
ms.assetid: 29bfe8ec-ca12-8fbf-b62b-ece3710dfe2e
description: '[レイアウトの構成] ダイアログ ボックスで図形をレイアウトするときにページに図形を配置する方法を指定します ([デザイン] タブの [レイアウト] グループで、[Re-Layout ページ] をクリックし、[その他のレイアウト オプション] をクリックします)。 VisCellIndices のレイアウト スタイルと配置の値を格納します。'
ms.openlocfilehash: e3347c25559191c5605dd70d8461680e1134d3bd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549624"
---
# <a name="shapeplacestyle-cell-shape-layout-section"></a>[ShapePlaceStyle] セル ([Shape Layout] セクション)

[レイアウトの構成] ダイアログ ボックスで図形をレイアウトするときにページに図形を配置する方法を指定します ([デザイン] タブの[レイアウト] グループで、[再レイアウト ページ] をクリックし、[その他のレイアウト オプション] をクリックします)。    **VisCellIndices** からレイアウト スタイルと整列の値を設定します。 
  
|**定数**|**値**|
|:-----|:-----|
|**visLOPlaceBottomToTop** <br/> |4   <br/> |
|**visLOPlaceCircular** <br/> |6   <br/> |
|**visLOPlaceCompactDownLeft** <br/> |14   <br/> |
|**visLOPlaceCompactDownRight** <br/> |7   <br/> |
|**visLOPlaceCompactLeftDown** <br/> |13  <br/> |
|**visLOPlaceCompactLeftUp** <br/> |12   <br/> |
|**visLOPlaceCompactRightDown** <br/> |8   <br/> |
|**visLOPlaceCompactRightUp** <br/> |9   <br/> |
|**visLOPlaceCompactUpLeft** <br/> |11  <br/> |
|**visLOPlaceCompactUpRight** <br/> |10  <br/> |
|**visLOPlaceDefault** <br/> |0  <br/> |
|**visLOPlaceHierarchyBottomToTopCenter** <br/> |20  <br/> |
|**visLOPlaceHierarchyBottomToTopLeft** <br/> |19  <br/> |
|**visLOPlaceHierarchyBottomToTopRight** <br/> | 21  <br/> |
|**visLOPlaceHierarchyLeftToRightBottom** <br/> |24  <br/> |
|**visLOPlaceHierarchyLeftToRightMiddle** <br/> |23  <br/> |
|**visLOPlaceHierarchyLeftToRightTop** <br/> |22  <br/> |
|**visLOPlaceHierarchyRightToLeftBottom** <br/> |27  <br/> |
|**visLOPlaceHierarchyRightToLeftMiddle** <br/> |26  <br/> |
|**visLOPlaceHierarchyRightToLeftTop** <br/> |25  <br/> |
|**visLOPlaceHierarchyTopToBottomCenter** <br/> |17   <br/> |
|**visLOPlaceHierarchyTopToBottomLeft** <br/> |16   <br/> |
|**visLOPlaceHierarchyTopToBottomRight** <br/> |18   <br/> |
|**visLOPlaceLeftToRight** <br/> |2  <br/> |
|**visLOPlaceParentDefault** <br/> |15   <br/> |
|**visLOPlaceRadial** <br/> |3  <br/> |
|**visLOPlaceRightToLeft** <br/> |5  <br/> |
|**visLOPlaceTopToBottom** <br/> |1  <br/> |
   
別の数式または  **CellsU** プロパティを使用したプログラムから、名前によって [ShapePlaceStyle] セルを参照するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |ShapePlaceStyle  <br/> |
   
プログラムから、インデックスによって [ShapePlaceStyle] セルを参照するには、 **CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visSLOPlaceStyle** <br/> |
   

