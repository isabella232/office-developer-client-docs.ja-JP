---
title: '[SelectMode] セル ([Group Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm875
localization_priority: Normal
ms.assetid: 5ba68e05-f394-d7b7-390d-f0a9fdad011e
description: グループ図形とそのメンバーを選択する方法を指定します。
ms.openlocfilehash: 82f9e2806d1131a0acfd064f585c681fef0f209f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326013"
---
# <a name="selectmode-cell-group-properties-section"></a>[SelectMode] セル ([Group Properties] セクション)

グループ図形とそのメンバーを選択する方法を指定します。
  
|**値**|**選択モード**|**オートメーション定数**|
|:-----|:-----|:-----|
|.0  <br/> |グループ図形だけを選択します。  <br/> |**visGrpSelModeGroupOnly** <br/> |
|1-d  <br/> |グループ図形を最初に選択します。  <br/> |**visGrpSelModeGroup1st** <br/> |
|pbm-2  <br/> |グループのメンバーを最初に選択します。  <br/> |**visGrpSelModeMembers1st** <br/> |
   
## <a name="remarks"></a>解説

この値は、[**基本動作**] ダイアログボックスで設定することもできます (グループ図形が選択されている状態)。 [[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] グループで、[**基本動作**] をクリックし、[グループ] の下にある**選択**リストでモードをクリックします。 **動作**)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [SelectMode] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |[selectmode]  <br/> |
   
プログラムから、インデックスによって [SelectMode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス :  <br/> |**visRowGroup** <br/> |
|セル インデックス:  <br/> |**visGroupSelectMode** <br/> |
   

