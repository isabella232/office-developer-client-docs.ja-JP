---
title: '[ShapeShdwOffsetX] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60076
localization_priority: Normal
ms.assetid: a426f471-d35f-ef87-4c59-2c007ec2653f
description: 図形の影を図形から水平方向にオフセットする距離を、ページの単位で指定します。
ms.openlocfilehash: 12512ce9edf49f91c786c3cd50baa8d07498a3de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806429"
---
# <a name="shapeshdwoffsetx-cell-fill-format-section"></a>[ShapeShdwOffsetX] セル ([Fill Format] セクション)

図形の影を図形から水平方向にオフセットする距離を、ページの単位で指定します。
  
## <a name="remarks"></a>注釈

この値は、[**影**] ダイアログ ボックスで設定する**X オフセット**の値に対応して ([**ホーム**] タブの [**図形**] グループで、**シャドウ**] をクリックし、[**影のオプション**] をクリック) します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShapeShdwOffsetX] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | ShapeShdwOffsetX  <br/> |
   
プログラムから、インデックスによって [ShapeShdwOffsetX] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowFill** <br/> |
| セル インデックス:  <br/> |**visFillShdwOffsetX** <br/> |
   

