---
title: '[PlaceStyle] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7dcd5a35-bd3d-447f-e4aa-986091d129de
description: '[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに、図形をページ上にどのように配置するかを指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] で [ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。'
ms.openlocfilehash: c2d0db15511d5e655318feeabfeb3bc2c29c0101
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623216"
---
# <a name="placestyle-cell-page-layout-section"></a>[PlaceStyle] セル ([Page Layout] セクション)

[**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトするときに、図形をページ上にどのように配置するかを指定します (このダイアログ ボックスを開くには、[**デザイン**] タブの [**レイアウト**] で [**ページの再レイアウト**] をクリックして、[**その他のレイアウト オプション**] をクリックします)。
  
## <a name="remarks"></a>注釈

このセルの値は、**[レイアウトの構成]** ダイアログ ボックスで設定することもできます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PlaceStyle] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |PlaceStyle  <br/> |
   
プログラムから、インデックスによって [PlaceStyle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOPlaceStyle** <br/> |
   

