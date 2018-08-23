---
title: '[LineJumpCode] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm540
localization_priority: Normal
ms.assetid: 56f9043d-a632-65df-c710-45867cce1627
description: 飛び越し点を表示するコネクタを指定します。
ms.openlocfilehash: abb7208c2cfbd6b1423e091efc1d526f8b10b57d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805698"
---
# <a name="linejumpcode-cell-page-layout-section"></a>[LineJumpCode] セル ([ページ レイアウト] セクション)

飛び越し点を表示するコネクタを指定します。
  
|**値**|**飛び越し点を表示するコネクタ**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |なし  <br/> |**visPLOJumpNone** <br/> |
|1  <br/> |横の線  <br/> |**visPLOJumpHorizontal** <br/> |
|2  <br/> |縦の線  <br/> |**visPLOJumpVertical** <br/> |
|3  <br/> |最後の経路  <br/> |**visPLOJumpLastRouted** <br/> |
|4  <br/> |最後に表示した線 ( *z*内の図形を上位の順)  <br/> |**visPLOJumpDisplayOrder** <br/> |
|5  <br/> |最初の行が表示されます ( *z*の一番下にある図形の順序)  <br/> |**visPLOJumpReverseDisplayOrder** <br/> |
   
## <a name="remarks"></a>注釈

このセルの値は、[**ページ設定**] ダイアログ ボックスの [**レイアウトと経路**] タブで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックして、[**レイアウトと経路**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineJumpCode] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |LineJumpCode  <br/> |
   
プログラムから、インデックスによって [LineJumpCode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOJumpCode** <br/> |
   

