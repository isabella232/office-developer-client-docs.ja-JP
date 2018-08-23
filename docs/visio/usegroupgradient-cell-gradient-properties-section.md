---
title: '[UseGroupGradient] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f1dcf0ec-8b4a-4ee1-9208-b1c84e30d37b
description: 図形が他の図形とグループ化されている場合、図形にグラデーションを適用するかどうかを、ブール演算型で決定します。[UseGroupGradient] セルの値が影響するのは、図形の塗りつぶしのみです。
ms.openlocfilehash: ca11ad1c54097b4883bb5348583c6cf39127e4e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806736"
---
# <a name="usegroupgradient-cell-gradient-properties-section"></a>[UseGroupGradient] セル ([グラデーションのプロパティ] セクション)

図形が他の図形とグループ化されている場合、図形にグラデーションを適用するかどうかを、ブール演算型で決定します。[**UseGroupGradient**] セルの値が影響するのは、図形の塗りつぶしのみです。 
  
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**UseGroupGradient**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | UseGroupGradient  <br/> |
   
プログラムから、インデックスによって [**UseGroupGradient**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowGradientProperties** <br/> |
| セル インデックス:  <br/> |* * visUseGroupGradient * * <br/> |
   

