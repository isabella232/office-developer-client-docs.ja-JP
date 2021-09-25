---
title: '[ResizePage] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm850
ms.localizationpriority: medium
ms.assetid: d63fe874-1027-3436-dbc1-73e722bce22e
description: '[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトした後で、図面が中心に位置するようにページを拡大するかどうかを指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] グループで、[ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。'
ms.openlocfilehash: 77fd339dd21c7f8111a7359ed8d293ddeee1111d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623076"
---
# <a name="resizepage-cell-page-layout-section"></a>[ResizePage] セル ([Page Layout] セクション)

[レイアウトの構成] ダイアログ ボックス ([デザイン] タブの [レイアウト]グループで、[レイアウトの再レイアウト] ページをクリックし、[その他のレイアウト オプション] をクリック) を使用して、図形をレイアウトした後に図面を囲むページを拡大するかどうかを指定します。  
  
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
   

