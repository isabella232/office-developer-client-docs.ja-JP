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
ms.openlocfilehash: 086685b47d8eaf170a8722f7cd00545230541e79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805231"
---
# <a name="displaymode-cell-group-properties-section"></a>[DisplayMode] セル ([グループのプロパティ] セクション)

グループ図形とそのメンバーの表示方法を指定します。
  
|**値**|**表示モード**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |グループ図形とテキストを表示しません。  <br/> |**visGrpDispModeNone** <br/> |
|1  <br/> |メンバー図形の背後にグループ図形を表示します。  <br/> |**visGrpDispModeBack** <br/> |
|2  <br/> |メンバー図形の手前にグループ図形を表示します。  <br/> |**visGrpDispModeFront** <br/> |
   
## <a name="remarks"></a>注釈

設定することもこの値、グループを選択すると [[開発](run-in-developer-mode-display-the-developer-tab.md)] タブで、**図形のデザイン**グループ**の動作**] をクリックし、**データをグループ化**] ボックスの一覧から表示モードを選択します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DisplayMode] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |DisplayMode  <br/> |
   
プログラムから、インデックスによって [DisplayMode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowGroup** <br/> |
|セル インデックス:  <br/> |**visGroupDisplayMode** <br/> |
   

