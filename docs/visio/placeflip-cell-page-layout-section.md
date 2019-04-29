---
title: '[PlaceFlip] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253251
localization_priority: Normal
ms.assetid: df014b98-cfd5-b6d3-4b8a-b0acb3b94412
description: '[レイアウトの構成] ダイアログ ボックスを使用するときに、配置可能な図形をページ上で反転または回転する方法を指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] グループで、[ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。'
ms.openlocfilehash: d1c31654782012b3536d35f3a12a923c2cc7a8f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434299"
---
# <a name="placeflip-cell-page-layout-section"></a>[PlaceFlip] セル ([Page Layout] セクション)

[**レイアウトの構成**] ダイアログ ボックスを使用するときに、配置可能な図形をページ上で反転または回転する方法を指定します (このダイアログ ボックスを開くには、[**デザイン**] タブの [**レイアウト**] グループで、[**ページの再レイアウト**] をクリックして、[**その他のレイアウト オプション**] をクリックします)。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|&amp;H0  <br/> |既定値です。 反転しません。  <br/> |**visLOFlipDefault** <br/> |
|&amp;H1  <br/> |水平方向に反転します。  <br/> |**visLOFlipX** <br/> |
|&amp;H2  <br/> |垂直方向に反転します。  <br/> |**visLOFlipY** <br/> |
|&amp;H4  <br/> |90°単位で回転します。  <br/> |**visLOFlipRotate** <br/> |
|&amp;H8  <br/> |反転しません。  <br/> |**visLOFlipNone** <br/> |
   
## <a name="remarks"></a>注釈

[PlaceFlip] セルの値を使用すると、配置可能な図形の向きを、接続先となっている隣接する配置可能な図形に合わせることができます。通常は、静的な接着を使用する図面をレイアウトする場合に使用されます。
  
特定の図形に対してこの動作を設定するには、[Shape Layout] セクションで [ShapePlaceFlip] セルを使用します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PlaceFilp] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[placeflip]  <br/> |
   
プログラムから、インデックスによって [PlaceFlip] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOPlaceFlip** <br/> |
   

