---
title: '[DisplayMode] セル ([Group Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251623
localization_priority: Normal
ms.assetid: e6d72529-aa03-e94b-130c-79ed04336299
description: グループ図形とそのメンバーの表示方法を指定します。
ms.openlocfilehash: a49d7a38eac75a2845de0ca3ad22f7cbf79a63df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413186"
---
# <a name="displaymode-cell-group-properties-section"></a>[DisplayMode] セル ([Group Properties] セクション)

グループ図形とそのメンバーの表示方法を指定します。
  
|**値**|**表示モード**|**オートメーション定数**|
|:-----|:-----|:-----|
|.0  <br/> |グループ図形とテキストを表示しません。  <br/> |**visGrpDispModeNone** <br/> |
|1   <br/> |メンバー図形の背後にグループ図形を表示します。  <br/> |**visGrpDispModeBack** <br/> |
|2   <br/> |メンバー図形の手前にグループ図形を表示します。  <br/> |**visGrpDispModeFront** <br/> |
   
## <a name="remarks"></a>注釈

この値を設定するには、グループを選択し、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] グループで [**基本動作**] をクリックし、[**グループデータ**] ボックスの一覧から表示モードを選択することもできます。 
  
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
   

