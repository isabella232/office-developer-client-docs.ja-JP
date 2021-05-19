---
title: '[PageWidth] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251372
localization_priority: Normal
ms.assetid: b98c5bf3-10c8-7299-2836-3906d6a9135d
description: 印刷ページの幅を図面単位で指定します。
ms.openlocfilehash: 6d887cb4335d2725101db54ba2b1483ccf01cff4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434271"
---
# <a name="pagewidth-cell-page-properties-section"></a>[PageWidth] セル ([Page Properties] セクション)

印刷ページの幅を図面単位で指定します。
  
## <a name="remarks"></a>注釈

[ページ設定] ダイアログ ボックスの[ページ サイズ] タブ ([デザイン] タブの[ページ設定] 矢印をクリック) でページ幅を設定したり、マウスを使用して手動でページのサイズを変更したりすることもできます。 これを行うには、Ctrl キーを押しながらページの端をドラッグします。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PageWidth] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |PageWidth  <br/> |
   
プログラムから、インデックスによって [PageWidth] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPage** <br/> |
|セル インデックス:  <br/> |**visPageWidth** <br/> |
   

