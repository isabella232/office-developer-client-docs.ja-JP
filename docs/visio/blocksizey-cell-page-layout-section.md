---
title: '[BlockSizeY] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm110
ms.localizationpriority: medium
ms.assetid: be51e18e-ea49-0788-1a17-866090afb9f4
description: '[レイアウトの構成] ダイアログ ボックス ([デザイン] タブの [レイアウト] グループで、[Re-Layout ページ] をクリックし、[その他のレイアウト オプション] をクリックして、 [レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに、各図形が図面ページに収まる領域である垂直方向のブロック サイズを指定します。'
ms.openlocfilehash: 11a3c4d576f125bd6a7a731585845f4b816f3096
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598711"
---
# <a name="blocksizey-cell-page-layout-section"></a>[BlockSizeY] セル ([Page Layout] セクション)

[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに、各図形が図面ページに収まる必要がある垂直方向のブロック サイズを指定します ([デザイン]タブの [レイアウト] グループで、[再レイアウトページ] をクリックし、[その他のレイアウト オプション] をクリックします)。  
  
## <a name="remarks"></a>注釈

この値は、[**間隔と図形サイズの設定**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブの [**ページ設定**] グループの矢印をクリックし、[**レイアウトと経路**] タブをクリックして、[**間隔**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BlockSizeY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | BlockSizeY  <br/> |
   
プログラムから、インデックスによって [BlockSizeY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visPLOBlockSizeY** <br/> |
   

