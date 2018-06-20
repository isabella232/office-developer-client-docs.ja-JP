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
ms.openlocfilehash: 426b4a18bbd54887e4f60b92860a6c3846386671
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806363"
---
# <a name="selectmode-cell-group-properties-section"></a>[SelectMode] セル ([Group Properties] セクション)

グループ図形とそのメンバーを選択する方法を指定します。
  
|**値**|**選択モード**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |グループ図形だけを選択します。  <br/> |**visGrpSelModeGroupOnly** <br/> |
|1  <br/> |グループ図形を最初に選択します。  <br/> |**visGrpSelModeGroup1st** <br/> |
|2  <br/> |グループのメンバーを最初に選択します。  <br/> |**visGrpSelModeMembers1st** <br/> |
   
## <a name="remarks"></a>備考

**動作**] ダイアログ ボックスでこの値を設定することもできます (グループ図形を選択して、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] で、[**動作**] をクリックし、**グループの下**の選択**ボックスの一覧でモードをクリックし、動作**)。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[SelectMode] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |SelectMode  <br/> |
   
プログラムから、インデックスによって [SelectMode] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowGroup** <br/> |
|セル インデックス:  <br/> |**visGroupSelectMode** <br/> |
   

