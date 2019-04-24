---
title: '[ResizePage] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm850
localization_priority: Normal
ms.assetid: d63fe874-1027-3436-dbc1-73e722bce22e
description: '[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトした後で、図面が中心に位置するようにページを拡大するかどうかを指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] グループで、[ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。'
ms.openlocfilehash: 8d0001ce35808f8c5f11068ed78865ce992af5cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326825"
---
# <a name="resizepage-cell-page-layout-section"></a>[ResizePage] セル ([Page Layout] セクション)

[**レイアウトの構成**] ダイアログボックスを使用して図形をレイアウトした後に、ページを拡大するかどうかを指定します ([**デザイン**] タブの [**レイアウト**] グループで、[ページの**再レイアウト**] をクリックし、[その他のレイアウト] をクリックします)。 **オプション**)。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | ページを拡大します。  <br/> |
| FALSE  <br/> | ページを拡大しません。  <br/> |
   
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ResizePage] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [resizepage]  <br/> |
   
プログラムから、インデックスによって [ResizePage] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visploresizepage** <br/> |
   

