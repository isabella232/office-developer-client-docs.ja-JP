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
description: どのように配置可能な図形を指定する反転または回転して、ページ レイアウトの構成] ダイアログ ボックスを使用する場合 ([デザイン] タブの [レイアウト] で、再レイアウト] ページをクリックし、他のレイアウト オプションをクリックし、)。
ms.openlocfilehash: fb16849c7a496a4277133c68453d94d6fd2e67f8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805991"
---
# <a name="placeflip-cell-page-layout-section"></a>[PlaceFlip] セル ([Page Layout] セクション)

どのように配置可能な図形を指定する反転または回転して、ページ**レイアウトの構成**] ダイアログ ボックスを使用する場合 ([**デザイン**] タブの [**レイアウト**] で、**ページの再レイアウト**] をクリックし、**他のレイアウト オプション**をクリックし、)。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|&amp;H0  <br/> |既定値です。反転しません。  <br/> |**visLOFlipDefault** <br/> |
|&amp;H1  <br/> |水平方向に反転します。  <br/> |**visLOFlipX** <br/> |
|&amp;H2  <br/> |垂直方向に反転します。  <br/> |**visLOFlipY** <br/> |
|&amp;H4  <br/> |90°単位で回転します。  <br/> |**visLOFlipRotate** <br/> |
|&amp;H8  <br/> |反転しません。  <br/> |**visLOFlipNone** <br/> |
   
## <a name="remarks"></a>注釈

[PlaceFlip] セルの値を使用すると、配置可能な図形の向きを、接続先となっている隣接する配置可能な図形に合わせることができます。通常は、静的な接着を使用する図面をレイアウトする場合に使用されます。
  
特定の図形に対してこの動作を設定するには、[Shape Layout] セクションで [ShapePlaceFlip] セルを使用します。
  
取得する、[PlaceFlip] セルへの参照名で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |PlaceFlip  <br/> |
   
プログラムから、インデックスによって [PlaceFlip] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOPlaceFlip** <br/> |
   

