---
title: '[LineToLineY] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm570
localization_priority: Normal
ms.assetid: db9a8232-25c5-7087-2ae9-50470d0cf16e
description: 図面ページにあるすべてのコネクタ間の垂直方向のクリアランスを指定します。
ms.openlocfilehash: 781d166fe0b81cc2402fde2894cd1d0480a0895f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805714"
---
# <a name="linetoliney-cell-page-layout-section"></a>[LineToLineY] セル ([ページ レイアウト] セクション)

図面ページにあるすべてのコネクタ間の垂直方向のクリアランスを指定します。
  
## <a name="remarks"></a>注釈

このセルの値は、[**間隔と図形サイズの設定**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックし、[**レイアウトと経路**] をクリックして、[**間隔**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineToLineY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[Linetoliney]  <br/> |
   
プログラムから、インデックスによって [LineToLineY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOLineToLineY** <br/> |
   

