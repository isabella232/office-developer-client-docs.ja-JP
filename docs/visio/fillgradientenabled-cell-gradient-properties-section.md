---
title: '[FillGradientEnabled] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 80db9c0c-13c6-47de-967f-ade6e5899f14
description: この図形で塗りつぶしのグラデーションを有効にするかどうかを決定します。
ms.openlocfilehash: 628ea789b01f760d54c79b4d60ca8529648da2b3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590206"
---
# <a name="fillgradientenabled-cell-gradient-properties-section"></a>[FillGradientEnabled] セル ([グラデーションのプロパティ] セクション)

この図形で塗りつぶしのグラデーションを有効にするかどうかを決定します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |グラデーションの塗りつぶしは図形に表示されます。  <br/> |
|FALSE  <br/> |グラデーションの塗りつぶしは図形には表示されません。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**FillGradientEnabled**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | FillGradientEnabled  <br/> |
   
プログラムから、インデックスによって [**FillGradientEnabled**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowGradientProperties** <br/> |
| セル インデックス:  <br/> |**visFillGradientEnabled ** <br/> |
   

