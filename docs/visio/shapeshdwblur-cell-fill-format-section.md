---
title: '[ShapeShdwBlur] セル ([塗りつぶしの書式設定] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 90ace659-d979-43e1-ac64-25af3ec5d666
description: 図形の影のぼかしのサイズをポイント単位 (0.00 ~ 100.00) で指定します。
ms.openlocfilehash: ae559cbb183266dbba3ed0e98c98d24db71f3b58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424988"
---
# <a name="shapeshdwblur-cell-fill-format-section"></a>[ShapeShdwBlur] セル ([塗りつぶしの書式設定] セクション)

図形の影のぼかしのサイズをポイント単位 (0.00 ~ 100.00) で指定します。 
  
## <a name="remarks"></a>注釈

別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[shapeshdwblur]** ] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [shapeshdwblur]  <br/> |
   
プログラムから、インデックスによって [ **[shapeshdwblur]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowFill** <br/> |
| セル インデックス:  <br/> |**visFillShdwBlur** <br/> |
   

