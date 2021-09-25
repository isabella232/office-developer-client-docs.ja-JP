---
title: '[DisplayMode] セル ([Group Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251623
ms.localizationpriority: medium
ms.assetid: e6d72529-aa03-e94b-130c-79ed04336299
description: グループ図形とそのメンバーの表示方法を指定します。
ms.openlocfilehash: 22989d22d0e8792e609027662750c4e9f9da73fa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590339"
---
# <a name="displaymode-cell-group-properties-section"></a>[DisplayMode] セル ([Group Properties] セクション)

グループ図形とそのメンバーの表示方法を指定します。
  
|**値**|**表示モード**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |グループ図形とテキストを表示しません。  <br/> |**visGrpDispModeNone** <br/> |
|1  <br/> |メンバー図形の背後にグループ図形を表示します。  <br/> |**visGrpDispModeBack** <br/> |
|2  <br/> |メンバー図形の手前にグループ図形を表示します。  <br/> |**visGrpDispModeFront** <br/> |
   
## <a name="remarks"></a>注釈

この値を設定するには、グループを選択し、[開発]タブの [図形デザイン][](run-in-developer-mode-display-the-developer-tab.md)グループの [動作] をクリックし、[グループ データ] リストから表示モード **を選択** します。  
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DisplayMode] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |DisplayMode  <br/> |
   
プログラムから、インデックスによって [DisplayMode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス :  <br/> |**visRowGroup** <br/> |
|セル インデックス:  <br/> |**visGroupDisplayMode** <br/> |
   

