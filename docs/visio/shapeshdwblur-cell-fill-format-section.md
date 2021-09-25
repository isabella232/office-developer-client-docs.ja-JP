---
title: '[ShapeShdwBlur] セル ([塗りつぶしの書式設定] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 90ace659-d979-43e1-ac64-25af3ec5d666
description: 図形の影のぼかしのサイズをポイント (0.00 ~ 100.00) で指定します。
ms.openlocfilehash: 4d42e4ff1ed5ae3bd1c168f7cb5b6b13ff3c75bc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598137"
---
# <a name="shapeshdwblur-cell-fill-format-section"></a>[ShapeShdwBlur] セル ([塗りつぶしの書式設定] セクション)

図形の影のぼかしのサイズをポイント (0.00 ~ 100.00) で指定します。 
  
## <a name="remarks"></a>注釈

別の数式 **、Cell** 要素の **N** 属性の値、**または CellsU** プロパティを使用するプログラムから、名前によって **ShapeShdwBlur** セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ShapeShdwBlur  <br/> |
   
プログラムからインデックスによって **ShapeShdwBlur** セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowFill** <br/> |
| セル インデックス:  <br/> |**visFillShdwBlur** <br/> |
   

