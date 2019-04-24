---
title: '[LineGradientEnabled] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 276a661f-d14e-404a-a494-ae36601a8ce3
description: 線または図形の境界線で線のグラデーションを有効にするかどうかを決定します。
ms.openlocfilehash: 1d2b33275d26bb0c8e5550bcb7cf282c64d34544
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361139"
---
# <a name="linegradientenabled-cell-gradient-properties-section"></a>[LineGradientEnabled] セル ([グラデーションのプロパティ] セクション)

線または図形の境界線で線のグラデーションを有効にするかどうかを決定します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |グラデーションは、図形の線または境界線に表示されます。  <br/> |
|FALSE  <br/> |グラデーションは、図形の線または境界線に表示されません。  <br/> |
   
## <a name="remarks"></a>解説

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**LineGradientEnabled**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [linegradientenabled]  <br/> |
   
プログラムから、インデックスによって [**LineGradientEnabled**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowGradientProperties** <br/> |
| セル インデックス:  <br/> |**visLineGradientEnabled** <br/> |
   

