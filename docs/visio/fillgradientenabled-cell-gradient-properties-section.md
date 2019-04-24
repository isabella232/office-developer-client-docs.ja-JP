---
title: '[FillGradientEnabled] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80db9c0c-13c6-47de-967f-ade6e5899f14
description: この図形で塗りつぶしのグラデーションを有効にするかどうかを決定します。
ms.openlocfilehash: 17f617c13b632318be22b86a3354a194f0f835f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322492"
---
# <a name="fillgradientenabled-cell-gradient-properties-section"></a>[FillGradientEnabled] セル ([グラデーションのプロパティ] セクション)

この図形で塗りつぶしのグラデーションを有効にするかどうかを決定します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |グラデーションの塗りつぶしは図形に表示されます。  <br/> |
|FALSE  <br/> |グラデーションの塗りつぶしは図形には表示されません。  <br/> |
   
## <a name="remarks"></a>解説

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**FillGradientEnabled**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [fillgradientenabled]  <br/> |
   
プログラムから、インデックスによって [**FillGradientEnabled**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowGradientProperties** <br/> |
| セル インデックス:  <br/> |* * visFillGradientEnabled * * <br/> |
   

