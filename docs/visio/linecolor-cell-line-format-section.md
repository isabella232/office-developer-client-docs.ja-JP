---
title: '[LineColor] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm535
localization_priority: Normal
ms.assetid: d857b48b-9a3d-a1e1-5ad2-6816a492c8ab
description: 図形の線の色を指定します。
ms.openlocfilehash: 6086a45108b88475e250c4d833ab4b740f33b8e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805705"
---
# <a name="linecolor-cell-line-format-section"></a>[LineColor] セル ([線の書式設定] セクション)

図形の線の色を指定します。
  
## <a name="remarks"></a>注釈

線の色を設定するには、線の色のコレクション内でインデックスとなっている 0 ～ 23 の数値を入力します。線の色のコレクションは、[**線**] ダイアログ ボックスで参照できます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**線**] をクリックし、[**太さ**] をポイントして、[**その他の線**] をクリックします)。[LineColor] の値は、[**線**] ダイアログ ボックスで設定することもできます。 
  
独自の色を入力するには、RGB または HSL 関数を使用します。 その RGB カラーでは、ユーザー設定の色の値と、数値ではなく RGB ( *r, g, b*)、[シェイプ シート] ウィンドウが表示されます。 数値演算で使用する場合は、24 以上の値があるユーザー設定の色です。 
  
線の色の透過性を設定するには、[LineColorTrans] セルを使用します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineColor] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |線の色  <br/> |
   
プログラムから、インデックスによって [LineColor] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLine** <br/> |
|セル インデックス:  <br/> |**visLineColor** <br/> |
   

