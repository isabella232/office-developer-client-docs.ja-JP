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
ms.openlocfilehash: fab37ee4561ba82ea1f314ad595e513253478b30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806230"
---
# <a name="resizepage-cell-page-layout-section"></a>[ResizePage] セル ([ページ レイアウト] セクション)

**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトした後で、図面ページを拡大するかどうか ([**デザイン**] タブの [**レイアウト**] で、**再レイアウト**] ページをクリックし、**以上のレイアウト] をクリックし、オプション**)。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | ページを拡大します。  <br/> |
| FALSE  <br/> | ページを拡大しません。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ResizePage] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ResizePage  <br/> |
   
プログラムから、インデックスによって [ResizePage] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visPLOResizePage** <br/> |
   

