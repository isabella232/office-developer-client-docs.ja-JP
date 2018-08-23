---
title: '[FillGradientEnabled] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80db9c0c-13c6-47de-967f-ade6e5899f14
description: この図形で塗りつぶしのグラデーションを有効にするかどうかを決定します。
ms.openlocfilehash: 20a38d4c45af163bc00364a45dc31269bf97251f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805389"
---
# <a name="fillgradientenabled-cell-gradient-properties-section"></a>[FillGradientEnabled] セル ([グラデーションのプロパティ] セクション)

この図形で塗りつぶしのグラデーションを有効にするかどうかを決定します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |グラデーションの塗りつぶしは図形に表示されます。  <br/> |
|FALSE  <br/> |グラデーションの塗りつぶしは図形には表示されません。  <br/> |
   
## <a name="remarks"></a>Remarks

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**FillGradientEnabled**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | FillGradientEnabled  <br/> |
   
プログラムから、インデックスによって [**FillGradientEnabled**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowGradientProperties** <br/> |
| セル インデックス:  <br/> |* * visFillGradientEnabled * * <br/> |
   

