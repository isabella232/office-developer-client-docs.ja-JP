---
title: '[UseGroupGradient] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f1dcf0ec-8b4a-4ee1-9208-b1c84e30d37b
description: ブール値として、他の図形と図形がグループ化されたときに図形のグラデーションにされるかどうかを決定します。 UseGroupGradient のセルの値は、図形の塗りつぶしのみに影響します。
ms.openlocfilehash: ca11ad1c54097b4883bb5348583c6cf39127e4e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806736"
---
# <a name="usegroupgradient-cell-gradient-properties-section"></a>[UseGroupGradient] セル ([グラデーションのプロパティ] セクション)

ブール値として、他の図形と図形がグループ化されたときに図形のグラデーションにされるかどうかを決定します。 **UseGroupGradient**のセルの値は、図形の塗りつぶしのみに影響します。 
  
## <a name="remarks"></a>備考

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **UseGroupGradient** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | UseGroupGradient  <br/> |
   
プログラムから、インデックスによって [ **UseGroupGradient** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowGradientProperties** <br/> |
| セル インデックス:  <br/> |* * visUseGroupGradient * * <br/> |
   

