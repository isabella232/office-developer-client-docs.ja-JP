---
title: '[ShapeShdwOffsetX] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60076
ms.localizationpriority: medium
ms.assetid: a426f471-d35f-ef87-4c59-2c007ec2653f
description: 図形の影を図形から水平方向にオフセットする距離を、ページの単位で指定します。
ms.openlocfilehash: 44a30995953f8fe01cf0e28ba180d0612ddb2fdb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570086"
---
# <a name="shapeshdwoffsetx-cell-fill-format-section"></a>[ShapeShdwOffsetX] セル ([Fill Format] セクション)

図形の影を図形から水平方向にオフセットする距離を、ページの単位で指定します。
  
## <a name="remarks"></a>注釈

この値は、[**影**] ダイアログ ボックスの [**X オフセット**] 設定の値に対応しています (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**影**] をクリックして、[**影のオプション**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapeShdwOffsetX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | ShapeShdwOffsetX  <br/> |
   
プログラムから、インデックスによって [ShapeShdwOffsetX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowFill** <br/> |
| セル インデックス:  <br/> |**visFillShdwOffsetX** <br/> |
   

