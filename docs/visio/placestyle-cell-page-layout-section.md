---
title: '[PlaceStyle] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dcd5a35-bd3d-447f-e4aa-986091d129de
description: '[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに、図形をページ上にどのように配置するかを指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] で [ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。'
ms.openlocfilehash: b3159b765922d6656d12dd42a377322e4a91fc04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346866"
---
# <a name="placestyle-cell-page-layout-section"></a>[PlaceStyle] セル ([Page Layout] セクション)

[**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトするときに、図形をページ上にどのように配置するかを指定します (このダイアログ ボックスを開くには、[**デザイン**] タブの [**レイアウト**] で [**ページの再レイアウト**] をクリックして、[**その他のレイアウト オプション**] をクリックします)。
  
## <a name="remarks"></a>解説

このセルの値は、**[レイアウトの構成]** ダイアログ ボックスで設定することもできます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PlaceStyle] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[placestyle]  <br/> |
   
プログラムから、インデックスによって [PlaceStyle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOPlaceStyle** <br/> |
   

