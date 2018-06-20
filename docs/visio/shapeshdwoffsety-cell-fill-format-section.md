---
title: '[ShapeShdwOffsetY] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60077
localization_priority: Normal
ms.assetid: ef200f41-7b69-1291-f9df-a7035239a033
description: 図形の影を図形から垂直方向にオフセットする距離を、ページの単位で指定します。
ms.openlocfilehash: 669e15fd1badf9cf76decb117a9c4fb91e731271
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806419"
---
# <a name="shapeshdwoffsety-cell-fill-format-section"></a>[ShapeShdwOffsetY] セル ([Fill Format] セクション)

図形の影を図形から垂直方向にオフセットする距離を、ページの単位で指定します。
  
## <a name="remarks"></a>注釈

この値は、[**影**] ダイアログ ボックスで設定する**Y のオフセット**値に対応する ([**ホーム**] タブの [**図形**] グループで、**シャドウ**] をクリックし、[**影のオプション**] をクリック) します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShapeShdwOffsetY] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | ShapeShdwOffsetY  <br/> |
   
プログラムから、インデックスによって [ShapeShdwOffsetY] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowFill** <br/> |
| セル インデックス:  <br/> |**visFillShdwOffsetY** <br/> |
   

