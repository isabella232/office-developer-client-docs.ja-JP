---
title: '[ShapePlaceStyle] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm70007
localization_priority: Normal
ms.assetid: 29bfe8ec-ca12-8fbf-b62b-ece3710dfe2e
description: '[レイアウトの構成] ダイアログボックスで図形をレイアウトするときに、図形をページに配置する方法を指定します ([デザイン] タブの [レイアウト] で [ページの再レイアウト] をクリックし、[その他のレイアウトオプション] をクリックします)。 レイアウトスタイルと配置値を VisCellIndices から格納します。'
ms.openlocfilehash: 381f74912b64395f33a2dc55c0bad24d36a16286
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326510"
---
# <a name="shapeplacestyle-cell-shape-layout-section"></a>[ShapePlaceStyle] セル ([Shape Layout] セクション)

[**レイアウトの構成**] ダイアログボックスで図形をレイアウトするときに、図形をページに配置する方法を指定します ([**デザイン**] タブの [**レイアウト**] で [**ページの再レイアウト**] をクリックし、[その**他のレイアウトオプション**] をクリックします)。 **VisCellIndices** からレイアウト スタイルと整列の値を設定します。 
  
|**定数**|**値**|
|:-----|:-----|
|**visLOPlaceBottomToTop** <br/> |2/4  <br/> |
|**visLOPlaceCircular** <br/> |シックス  <br/> |
|**visLOPlaceCompactDownLeft** <br/> |第  <br/> |
|**visLOPlaceCompactDownRight** <br/> |7  <br/> |
|**visLOPlaceCompactLeftDown** <br/> |スリー  <br/> |
|**visLOPlaceCompactLeftUp** <br/> |個  <br/> |
|**visLOPlaceCompactRightDown** <br/> |~  <br/> |
|**visLOPlaceCompactRightUp** <br/> |i-9  <br/> |
|**visLOPlaceCompactUpLeft** <br/> |#  <br/> |
|**visLOPlaceCompactUpRight** <br/> |個  <br/> |
|**visLOPlaceDefault** <br/> |.0  <br/> |
|**visLOPlaceHierarchyBottomToTopCenter** <br/> |1280  <br/> |
|**visLOPlaceHierarchyBottomToTopLeft** <br/> |年  <br/> |
|**visLOPlaceHierarchyBottomToTopRight** <br/> |21  <br/> |
|**visLOPlaceHierarchyLeftToRightBottom** <br/> |ソケット  <br/> |
|**visLOPlaceHierarchyLeftToRightMiddle** <br/> |最高  <br/> |
|**visLOPlaceHierarchyLeftToRightTop** <br/> |×  <br/> |
|**visLOPlaceHierarchyRightToLeftBottom** <br/> |27  <br/> |
|**visLOPlaceHierarchyRightToLeftMiddle** <br/> |日  <br/> |
|**visLOPlaceHierarchyRightToLeftTop** <br/> |まで  <br/> |
|**visLOPlaceHierarchyTopToBottomCenter** <br/> |インチ  <br/> |
|**visLOPlaceHierarchyTopToBottomLeft** <br/> |16  <br/> |
|**visLOPlaceHierarchyTopToBottomRight** <br/> |個  <br/> |
|**visLOPlaceLeftToRight** <br/> |pbm-2  <br/> |
|**visLOPlaceParentDefault** <br/> |約  <br/> |
|**visLOPlaceRadial** <br/> |1/3  <br/> |
|**visLOPlaceRightToLeft** <br/> |5  <br/> |
|**visLOPlaceTopToBottom** <br/> |1-d  <br/> |
   
別の数式または  **CellsU** プロパティを使用したプログラムから、名前によって [ShapePlaceStyle] セルを参照するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[shapeplacestyle]  <br/> |
   
プログラムから、インデックスによって [ShapePlaceStyle] セルを参照するには、 **CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**vissloplace スタイル** <br/> |
   

