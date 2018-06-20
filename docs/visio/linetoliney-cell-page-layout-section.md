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
# <a name="linetoliney-cell-page-layout-section"></a>[LineToLineY] セル ([Page Layout] セクション)

図面ページにあるすべてのコネクタ間の垂直方向のクリアランスを指定します。
  
## <a name="remarks"></a>注釈

**レイアウトと間隔**] ダイアログ ボックスで、このセルの値を設定することもできます。 ([**デザイン**] タブで、**ページ設定**の矢印をクリックして、[**レイアウトと経路**、および、[**間隔**] をクリックします。)
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [linetoliney] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[Linetoliney]  <br/> |
   
プログラムから、インデックスによって [linetoliney] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOLineToLineY** <br/> |
   

