---
title: '[IsDropTarget] セル ([Group Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm495
localization_priority: Normal
ms.assetid: 8140fc7b-b99c-54bb-7af3-7de6fcdae7d3
description: グループにドロップされた図形を、そのグループが受け入れるかどうかを決定します。
ms.openlocfilehash: 50f545b3cbd4f7e1541a7f5e8ca32c34d0429c5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297229"
---
# <a name="isdroptarget-cell-group-properties-section"></a>[IsDropTarget] セル ([Group Properties] セクション)

グループにドロップされた図形を、そのグループが受け入れるかどうかを決定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |グループは、ドロップされた図形を受け入れます。  <br/> |
|FALSE  <br/> |グループは、ドロップされた図形を受け入れません。  <br/> |
   
## <a name="remarks"></a>解説

このセルの値は、グループを選択して、[[開発者用](run-in-developer-mode-display-the-developer-tab.md)] タブの [**基本動作**] をクリックし、[**ドロップした図形を受け入れる**] チェック ボックスをオンにして設定することもできます。 
  
図形をグループ上にドロップしてそのグループに追加するには、図形に対してもこの動作を有効にする必要があります。有効にするには、図形を選択して [[開発者用](run-in-developer-mode-display-the-developer-tab.md)] タブの [**基本動作**] をクリックし、[**ドロップ時にグループに図形を追加**] チェック ボックスをオンにします。この値は、[Miscellaneous] セクションの [IsDropSource] セルに格納されます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [IsDropTarget] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[isdroptarget]  <br/> |
   
プログラムから、インデックスによって [IsDropTarget] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス :  <br/> |**visRowGroup** <br/> |
|セル インデックス:  <br/> |**visGroupIsDropTarget** <br/> |
   

