---
title: '[ConFixedCode] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm175
localization_priority: Normal
ms.assetid: 8e7c9080-7ef1-0696-a3d2-d8f57ea5ab9b
description: コネクタの経路の変更方法を指定します。
ms.openlocfilehash: b2b9cde309c720493f0e46962b2fe6c2e79545d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404184"
---
# <a name="confixedcode-cell-shape-layout-section"></a>[ConFixedCode] セル ([Shape Layout] セクション)

コネクタの経路の変更方法を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|.0  <br/> |自由に経路を変更します。  <br/> |**visSLOConFixedRerouteFreely** <br/> |
|1   <br/> |必要に応じて経路を再設定します (手動による変更)。  <br/> |**visSLOConFixedRerouteAsNeeded** <br/> |
|2   <br/> |経路変更しません。  <br/> |**visSLOConFixedRerouteNever** <br/> |
|3   <br/> |交差時に経路を変更します。  <br/> |**visSLOConFixedRerouteOnCrossover** <br/> |
|4   <br/> |システム内部でのみ使用します。  <br/> |**visSLOConFixedByAlgFrom** <br/> |
|5   <br/> |システム内部でのみ使用します。  <br/> |**visSLOConFixedByAlgTo** <br/> |
|6   <br/> |システム内部でのみ使用します。  <br/> |**visSLOConFixedByAlgFromTo** <br/> |
   
## <a name="remarks"></a>注釈

このセルの値は、動的コネクタを選択し、[[開発者用](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] で [**基本動作**] をクリックし、[**コネクタ**] タブをクリックして設定することもできます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ConFixedCode] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[confixedcode]  <br/> |
   
プログラムから、インデックスによって [ConFixedCode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visslo# xedcode** <br/> |
   

