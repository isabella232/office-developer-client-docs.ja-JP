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
ms.openlocfilehash: 0624ec42978292e84965c978d25e4052fc41613f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806263"
---
# <a name="rounding-cell-line-format-section"></a>[Rounding] セル ([線の書式設定] セクション)

1 つのパス上で接する 2 つの連続したセグメントに適用される、円弧の半径を示します。たとえば、このセルを使用すると、四角形の角を丸くできます。丸みを設定するには、値と単位を入力します (数値と単位を組み合わせる)。
  
## <a name="remarks"></a>注釈

**線**] ダイアログ ボックスでこの値を設定することもできます ([**ホーム**] タブの [**図形**] グループで、[**行**] をクリックして、[**太さ**] をポイントおよび**他の線**] をクリック) します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Rounding] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Rounding  <br/> |
   
プログラムから、インデックスによって [Rounding] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLine** <br/> |
|セル インデックス:  <br/> |**visLineRounding** <br/> |
   

