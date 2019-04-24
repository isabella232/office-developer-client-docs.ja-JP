---
title: '[ShapeSplit] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60080
localization_priority: Normal
ms.assetid: 96b8c503-67b3-8623-d99b-0dad7b15c224
description: この図形が、分割可能な図形を分割できるかどうかを示します。
ms.openlocfilehash: 46b42e9be070b54095d3e9a5c247d63be6348f77
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349120"
---
# <a name="shapesplit-cell-shape-layout-section"></a>[ShapeSplit] セル ([Shape Layout] セクション)

この図形が、分割可能な図形を分割できるかどうかを示します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| .0  <br/> | この図形は他の図形を分割できません。  <br/> |**visslosplitnone** <br/> |
| 1-d  <br/> | この図形は他の図形を分割できます。  <br/> |**visslosplitallow** <br/> |
   
## <a name="remarks"></a>解説

他の図形を分割できる図形は、2 次元図形か 1 次元の配置可能な図形のどちらかである必要があります。 
  
図形の自動分割は、アプリケーション、ページ、および図形の 3 つのレベルで有効または無効にできます。既定では、アプリケーション レベルとページ レベルで分割できます。図形レベルでは、図面の種類によって異なります。 
  
アプリケーションレベルで分割を有効または無効にするには、[ **Visio のオプション**] ダイアログボックスの [**詳細**設定] タブで、[**コネクタ分割の有効化**] 設定を使用します ([**ファイル**] タブをクリックし、[**オプション**] をクリックして **、[詳細**)。 
  
ページで分割を有効または無効にするには、[PageShapeSplit] セルを使用します。 
  
1 次元図形を分割可能にするには、[ShapeSplittable] セルを使用します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [参照] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [shapesplit]  <br/> |
   
プログラムから、インデックスによって [ShapeSplit] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowShapeLayout** <br/> |
| セル インデックス:  <br/> |**visslosplit** <br/> |
   

