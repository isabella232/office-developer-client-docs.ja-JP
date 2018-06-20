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
# <a name="conlinejumpcode-cell-shape-layout-section"></a>[ConLineJumpCode] セル ([Shape Layout] セクション)

コネクタの飛び越し点の表示方法を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |ページで指定します。[**デザイン**] タブで、[**ページ設定**] で矢印をクリックし **、レイアウトと経路**] タブにページの仕様を参照してください。  <br/> |**visSLOJumpDefault** <br/> |
|1  <br/> |Never/なし  <br/> |**visSLOJumpNever** <br/> |
|2  <br/> |Always/印刷/画面  <br/> |**visSLOJumpAlways** <br/> |
|3  <br/> |常に相手側に表示します。  <br/> |**visSLOJumpOther** <br/> |
|4  <br/> |どちらのコネクタに飛び越し点します。  <br/> |**visSLOJumpNeither** <br/> |
   
## <a name="remarks"></a>備考

設定できますでは、このセルの値、動的コネクタを**図形のデザイン**] で [[開発](run-in-developer-mode-display-the-developer-tab.md)] タブで、**動作**をクリックして、[**コネクタ**] タブをクリックします。 
  
取得する、[ConLineJumpCode] セルへの参照名で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |ConLineJumpCode  <br/> |
   
プログラムから、インデックスによって [ConLineJumpCode] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visSLOJumpCode** <br/> |
   

