---
title: '[ConLineJumpCode] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251652
localization_priority: Normal
ms.assetid: af85588e-8e83-5168-7a8c-d7e8b4af5c27
description: コネクタの飛び越し点の表示方法を指定します。
ms.openlocfilehash: 002f628841356ec8a22afbb9d4aeca8236058222
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805089"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a>[ConLineJumpCode] セル ([図形レイアウト] セクション)

コネクタの飛び越し点の表示方法を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |
          ページの指定に合わせます。[**デザイン**] タブの [**ページ設定**] グループの矢印をクリックして、[**レイアウトと経路**] タブをクリックするとページの指定内容を参照できます。
  <br/> |**visSLOJumpDefault** <br/> |
|1  <br/> |Never/なし  <br/> |**visSLOJumpNever** <br/> |
|2  <br/> |Always/印刷/画面  <br/> |**visSLOJumpAlways** <br/> |
|3  <br/> |常に相手側に表示します。  <br/> |**visSLOJumpOther** <br/> |
|4  <br/> |
          どちらの側にも表示しません。
  <br/> |**visSLOJumpNeither** <br/> |
   
## <a name="remarks"></a>注釈

設定できますでは、このセルの値、動的コネクタを**図形のデザイン**] で [[開発](run-in-developer-mode-display-the-developer-tab.md)] タブで、**動作**をクリックして、[**コネクタ**] タブをクリックします。 
  
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
   

