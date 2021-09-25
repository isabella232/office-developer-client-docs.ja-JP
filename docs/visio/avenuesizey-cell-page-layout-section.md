---
title: '[AvenueSizeY] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm70
ms.localizationpriority: medium
ms.assetid: 9ff2893c-afe5-505e-0b55-48ec1de08a5f
description: '[レイアウトの構成] ダイアログ ボックス ([デザイン] タブの [レイアウト] グループで、[ Re-Layout ページ] をクリックし、[ その他のレイアウト オプション] をクリックして) 図形をレイアウトするときに、図面ページ上の図形間の垂直スペースの量を指定します。'
ms.openlocfilehash: 08c40814735f4e2db8092221c99f9213857f14ec
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578187"
---
# <a name="avenuesizey-cell-page-layout-section"></a>[AvenueSizeY] セル ([Page Layout] セクション)

[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに図面ページ上の図形間の垂直方向の領域の量を指定します ([デザイン]タブの [レイアウト] グループで、[レイアウトの再レイアウト ページ] をクリックし、[その他のレイアウト オプション] をクリックします)。   
  
## <a name="remarks"></a>注釈

この値は、[**間隔と図形サイズの設定**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブの [**ページ設定**] グループの矢印をクリックし、[**レイアウトと経路**] タブをクリックして、[**間隔**] をクリックします)。
  
ダイナミック グリッドでは、上下の間隔の計算対象となる図形が 1 つだけある場合に [AvenueSizeY] セルの設定が使用されます。ダイナミック グリッドを使用するには、[**表示**] タブの [**視覚的補助**] グループで、[**ダイナミック グリッド**] チェック ボックスをオンにします。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AvenueSizeY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | AvenueSizeY  <br/> |
   
プログラムから、インデックスによって [AvenueSizeY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visPLOAvenueSizeY** <br/> |
   

