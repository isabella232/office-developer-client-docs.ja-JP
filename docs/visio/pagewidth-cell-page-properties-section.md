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
ms.openlocfilehash: e03696c8f1c921c930d3563e9c73ef4ae613a7c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805979"
---
# <a name="pagewidth-cell-page-properties-section"></a>[PageWidth] セル ([ページのプロパティ] セクション)

印刷ページの幅を図面単位で指定します。
  
## <a name="remarks"></a>注釈

**[ページ設定**] ダイアログ ボックスの [**ページ サイズ**] タブで、ページの幅を設定することも ([**デザイン**] タブで、矢印をクリック、 **[ページ設定**) または手動でマウスを使用してページ サイズを変更しています。 これを行うには、CTRL キーを押しながら、ページの端をドラッグします。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PageWidth] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[Pagewidth]  <br/> |
   
プログラムから、インデックスによって [PageWidth] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPage** <br/> |
|セル インデックス:  <br/> |**visPageWidth** <br/> |
   

