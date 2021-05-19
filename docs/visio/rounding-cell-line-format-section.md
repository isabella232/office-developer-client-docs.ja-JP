---
title: '[Rounding] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm860
localization_priority: Normal
ms.assetid: c44457ca-997a-5315-44dd-4218e4203550
description: 1 つのパス上で接する 2 つの連続したセグメントに適用される、円弧の半径を示します。たとえば、このセルを使用すると、四角形の角を丸くできます。丸みを設定するには、値と単位を入力します (数値と単位を組み合わせる)。
ms.openlocfilehash: d64d3266e3dd2b0a3998955efe271aab04905fbf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427011"
---
# <a name="rounding-cell-line-format-section"></a>[Rounding] セル ([Line Format] セクション)

1 つのパス上で接する 2 つの連続したセグメントに適用される、円弧の半径を示します。たとえば、このセルを使用すると、四角形の角を丸くできます。丸みを設定するには、値と単位を入力します (数値と単位を組み合わせる)。
  
## <a name="remarks"></a>注釈

[線] ダイアログ ボックスでこの値を設定することもできます([ホーム] タブの [図形] グループで、[線]**をクリック** し、[太さ] をポイントし、[その他の線] を **クリックします**)。  
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Rounding] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |丸めの方法  <br/> |
   
プログラムから、インデックスによって [Rounding] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLine** <br/> |
|セル インデックス:  <br/> |**visLineRounding** <br/> |
   

