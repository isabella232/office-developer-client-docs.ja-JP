---
title: '[EndArrowSize] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251630
localization_priority: Normal
ms.assetid: e2ecf7c0-a0e9-951f-676a-8e5857bb6544
description: 線の終端にある矢印のサイズを指定します。
ms.openlocfilehash: e03871c75857297634300c2eee091de2d0144903
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805331"
---
# <a name="endarrowsize-cell-line-format-section"></a>[EndArrowSize] セル ([Line Format] セクション)

線の終端にある矢印のサイズを指定します。
  
|**値**|**Size**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |極小  <br/> |**visArrowSizeVerySmall** <br/> |
|1  <br/> |小  <br/> |**visArrowSizeSmall** <br/> |
|2  <br/> |中  <br/> |**visArrowSizeMedium** <br/> |
|3  <br/> |大  <br/> |**visArrowSizeLarge** <br/> |
|4  <br/> |特大  <br/> |**visArrowSizeVeryLarge** <br/> |
|5  <br/> |超特大  <br/> |**visArrowSizeJumbo** <br/> |
|6  <br/> |巨大  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>備考

**線**] ダイアログ ボックスでこの値を設定することもできます ([**ホーム**] タブの [**図形**] グループで、[**行**] をクリックして、**矢印**] をポイントし、**複数の矢印**をクリックして)。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[EndArrowSize] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |EndArrowSize  <br/> |
   
プログラムから、インデックスによって [EndArrowSize] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLine** <br/> |
|セル インデックス:  <br/> |**visLineEndArrowSize** <br/> |
   

