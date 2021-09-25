---
title: '[ConLineJumpCode] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251652
ms.localizationpriority: medium
ms.assetid: af85588e-8e83-5168-7a8c-d7e8b4af5c27
description: コネクタの飛び越し点の表示方法を指定します。
ms.openlocfilehash: e1caea1f839bb139c41051f288c7e6b160767768
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582912"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a>[ConLineJumpCode] セル ([Shape Layout] セクション)

コネクタの飛び越し点の表示方法を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |
          ページの指定に合わせます。[**デザイン**] タブの [**ページ設定**] グループの矢印をクリックして、[**レイアウトと経路**] タブをクリックするとページの指定内容を参照できます。
  <br/> |**visSLOJumpDefault** <br/> |
|1  <br/> |Never  <br/> |**visSLOJumpNever** <br/> |
|2  <br/> |常時  <br/> |**visSLOJumpAlways** <br/> |
|3  <br/> |常に相手側に表示します。  <br/> |**visSLOJumpOther** <br/> |
|4   <br/> |どちらの側にも表示しません。  <br/> |**visSLOJumpNeither** <br/> |
   
## <a name="remarks"></a>注釈

このセルの値を設定するには、動的コネクタを選択し、[開発] タブの [図形デザイン] グループ [](run-in-developer-mode-display-the-developer-tab.md)の [動作] をクリックし、[コネクタ] タブ **をクリック** します。  
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ConLineJumpCode] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |ConLineJumpCode  <br/> |
   
プログラムから、インデックスによって [ConLineJumpCode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visSLOJumpCode** <br/> |
   

