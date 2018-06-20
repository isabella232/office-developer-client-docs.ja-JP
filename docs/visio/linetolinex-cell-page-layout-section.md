---
title: '[LineToLineX] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm565
localization_priority: Normal
ms.assetid: f6b461fe-56ac-4c0e-31cd-6b3c1075db6e
description: 図面ページにあるすべてのコネクタ間の水平方向のクリアランスを指定します。
ms.openlocfilehash: aa6476eab9d5bcf7aab12235fd23f0f5675d6ad5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805709"
---
# <a name="linetolinex-cell-page-layout-section"></a>[LineToLineX] セル ([Page Layout] セクション)

図面ページにあるすべてのコネクタ間の水平方向のクリアランスを指定します。
  
## <a name="remarks"></a>注釈

**レイアウトと間隔**] ダイアログ ボックスで、このセルの値を設定することもできます。 ([**デザイン**] タブで、**ページ設定**の矢印をクリックして、[**レイアウトと経路**、および、[**間隔**] をクリックします。)
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [linetolinex] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[Linetolinex]  <br/> |
   
プログラムから、インデックスによって [linetolinex] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOLineToLineX** <br/> |
   

