---
title: '[BlockSizeY] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm110
localization_priority: Normal
ms.assetid: be51e18e-ea49-0788-1a17-866090afb9f4
description: 図形の領域は、レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに図面ページに収まる必要があります、垂直方向のブロック サイズを指定 ([デザイン] タブの [レイアウト] で、再レイアウト] ページをクリックし、他のレイアウト オプションをクリックし、)。
ms.openlocfilehash: 283723bf902c07cfb044ab73107491df3c170a4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804913"
---
# <a name="blocksizey-cell-page-layout-section"></a>[BlockSizeY] セル ([ページ レイアウト] セクション)

図形の領域は、**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトするときに図面ページに収まる必要があります、垂直方向のブロック サイズを指定 ([**デザイン**] タブの [**レイアウト**] をクリックして **[再レイアウト] ページ**で、および**他のレイアウト オプション**] をクリック) します。
  
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
   

