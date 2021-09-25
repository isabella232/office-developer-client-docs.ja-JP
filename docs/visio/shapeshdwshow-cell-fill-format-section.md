---
title: '[ShapeShdwShow] セル ([塗りつぶしの書式設定] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: 図形に影を表示するかどうかを、0 から 2 の整数で決定します。
ms.openlocfilehash: 29e7d2a7c900518d933899cedc35a00dcc046e65
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598123"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a>[ShapeShdwShow] セル ([塗りつぶしの書式設定] セクション)

図形に影を表示するかどうかを、0 から 2 の整数で決定します。
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |影が指定されている場合は、常に影を表示します。サブ図形の影は表示されません。  <br/> |
|1  <br/> |図形の親が存在しない場合を除き、影を表示しません。共にグループ化されている場合は、サブ図形の影を使用します。  <br/> |
|2  <br/> |影が指定されている場合は、常に影を表示します。サブ図形の影も表示されます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**ShapeShdwShow**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ShapeShdwShow  <br/> |
   
プログラムから、インデックスによって [**ShapeShdwShow**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowFill** <br/> |
| セル インデックス:  <br/> |**visFillShdwShow** <br/> |
   

