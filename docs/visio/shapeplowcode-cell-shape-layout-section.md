---
title: '[ShapePlowCode] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm900
ms.localizationpriority: medium
ms.assetid: acf07fd7-6aa6-1a92-9b7a-bd6fea8a7cb2
description: 図面ページで、別の配置可能な図形をこの図形の近くにドロップしたときに、この図形を移動して遠ざけるかどうかを指定します。
ms.openlocfilehash: 53b13a7194bf723410e739b83378fd49e13022c6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622915"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a>[ShapePlowCode] セル ([Shape Layout] セクション)

図面ページで、別の配置可能な図形をこの図形の近くにドロップしたときに、この図形を移動して遠ざけるかどうかを指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |ページの指定に従って移動します。  <br/> |**visSLOPlowDefault** <br/> |
|1  <br/> |どの図形も移動しません。  <br/> |**visSLOPlowNever** <br/> |
|2  <br/> |すべての図形が移動します。  <br/> |**visSLOPlowAlways** <br/> |
   
## <a name="remarks"></a>注釈

[動作] ダイアログ ボックスの [配置] タブで、特定の図形のこのセルの値を設定することもできます (図形が選択されている場合は、[開発] タブの[図形のデザイン] グループで、[動作] をクリックし、[配置] タブを **クリック** します)。  [](run-in-developer-mode-display-the-developer-tab.md) 
  
図面ページのすべての  *図形に対*  してこの動作を設定するには、[ページ レイアウト] セクションの [PlowCode] セルを使用します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapePlowCode] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |ShapePlowCode  <br/> |
   
プログラムから、インデックスによって [ShapePlowCode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visSLOPlowCode** <br/> |
   

