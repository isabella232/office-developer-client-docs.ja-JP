---
title: '[UseGroupGradient] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f1dcf0ec-8b4a-4ee1-9208-b1c84e30d37b
description: 図形が他の図形とグループ化されている場合、図形にグラデーションを適用するかどうかを、ブール演算型で決定します。 [UseGroupGradient] セルの値が影響するのは、図形の塗りつぶしのみです。
ms.openlocfilehash: a69b48095aec93705c686a5401051f1d1e368d18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337157"
---
# <a name="usegroupgradient-cell-gradient-properties-section"></a>[UseGroupGradient] セル ([グラデーションのプロパティ] セクション)

図形が他の図形とグループ化されている場合、図形にグラデーションを適用するかどうかを、ブール演算型で決定します。 [**UseGroupGradient**] セルの値が影響するのは、図形の塗りつぶしのみです。 
  
## <a name="remarks"></a>解説

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**UseGroupGradient**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [usegroupgradient]  <br/> |
   
プログラムから、インデックスによって [**UseGroupGradient**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowGradientProperties** <br/> |
| セル インデックス:  <br/> |* * visUseGroupGradient * * <br/> |
   

