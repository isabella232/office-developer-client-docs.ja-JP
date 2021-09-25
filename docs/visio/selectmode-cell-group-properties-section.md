---
title: '[SelectMode] セル ([Group Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm875
ms.localizationpriority: medium
ms.assetid: 5ba68e05-f394-d7b7-390d-f0a9fdad011e
description: グループ図形とそのメンバーを選択する方法を指定します。
ms.openlocfilehash: e98e900afa6a6ca1ca166a08615c266c88df5457
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559620"
---
# <a name="selectmode-cell-group-properties-section"></a>[SelectMode] セル ([Group Properties] セクション)

グループ図形とそのメンバーを選択する方法を指定します。
  
|**値**|**選択モード**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |グループ図形だけを選択します。  <br/> |**visGrpSelModeGroupOnly** <br/> |
|1  <br/> |グループ図形を最初に選択します。  <br/> |**visGrpSelModeGroup1st** <br/> |
|2  <br/> |グループのメンバーを最初に選択します。  <br/> |**visGrpSelModeMembers1st** <br/> |
   
## <a name="remarks"></a>注釈

この値は、[動作] ダイアログボックスで設定することもできます (グループ図形が選択されている場合は、[開発]タブの [図形のデザイン] グループで、[動作]をクリックし、[グループの動作] の下の [選択] リストでモードをクリック **します**)。 [](run-in-developer-mode-display-the-developer-tab.md)  
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [SelectMode] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |SelectMode  <br/> |
   
プログラムから、インデックスによって [SelectMode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス :  <br/> |**visRowGroup** <br/> |
|セル インデックス:  <br/> |**visGroupSelectMode** <br/> |
   

