---
title: '[BlockSizeX] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm105
localization_priority: Normal
ms.assetid: 253aac17-077e-48e0-39a8-a3abd5d4a257
description: '[レイアウトの構成] ダイアログ ボックス ([デザイン] タブの [レイアウト] グループの [Re-Layout ページ] をクリックし、[その他のレイアウト オプション] をクリックして図形をレイアウトするときに、図面ページに図形が収まる必要がある領域である水平方向のブロック サイズを指定します。'
ms.openlocfilehash: 8e4cee4b2059d9b8f2fe77c2d4902e67246eac2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424190"
---
# <a name="blocksizex-cell-page-layout-section"></a>[BlockSizeX] セル ([Page Layout] セクション)

[レイアウトの構成] ダイアログ ボックス ([デザイン] タブの [レイアウト] グループの [レイアウト]グループで、[ レイアウトの再レイアウト] をクリックし、[ その他のレイアウト オプション] をクリック) を使用して図形をレイアウトするときに、各図形が図面ページに収まる領域である水平方向のブロック サイズを決定します。  
  
## <a name="remarks"></a>注釈

この値は、[**間隔と図形サイズの設定**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**デザイン**] タブの [**ページ設定**] グループの矢印をクリックし、[**レイアウトと経路**] タブをクリックして、[**間隔**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BlockSizeX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |BlockSizeX  <br/> |
   
プログラムから、インデックスによって [BlockSizeX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visPLOBlockSizeX** <br/> |
   

