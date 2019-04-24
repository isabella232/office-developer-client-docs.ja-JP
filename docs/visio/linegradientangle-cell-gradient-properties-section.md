---
title: '[LineGradientAngle] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b533ea0-5d2e-44fc-a691-8fa2f310ff9f
description: 線形グラデーションの線のグラデーションの角度を、0 ~ 359.9 度の角度で指定します。
ms.openlocfilehash: fd806bc7c953dbd86abd95c8e6103ab9e6ee1a10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359269"
---
# <a name="linegradientangle-cell-gradient-properties-section"></a>[LineGradientAngle] セル ([グラデーションのプロパティ] セクション)

線形グラデーションの線のグラデーションの角度を、0 ~ 359.9 度の角度で指定します。
  
## <a name="remarks"></a>解説

別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[linegradientangle]** ] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [linegradientangle]  <br/> |
   
プログラムから、インデックスによって [ **[linegradientangle]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowGradientProperties** <br/> |
| セル インデックス:  <br/> |**visLineGradientAngle** <br/> |
   

