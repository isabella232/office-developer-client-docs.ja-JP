---
title: '[ExtraInfo] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm360
localization_priority: Normal
ms.assetid: 55834445-8619-f79a-aea0-0f6a1780e016
description: イメージ マップの座標など、URL の解決に使用される情報を渡す文字列を表します。 ExtraInfo] セルで、x = 41&amp;y 7specifies のイメージ マップの座標を = します。
ms.openlocfilehash: aa035d5ec863cd8045063af970efa26b53683793
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805355"
---
# <a name="extrainfo-cell-hyperlinks-section"></a>[ExtraInfo] セル ([ハイパーリンク] セクション)

イメージ マップの座標など、URL の解決に使用される情報を渡す文字列を表します。 ExtraInfo] セルで、"x = 41&amp;y = 7"イメージ マップの座標を指定します。
  
## <a name="remarks"></a>備考

イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ExtraInfo] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ハイパーリンク  *名*です。ExtraInfo いるハイパーリンク。  *名前*は、行の名前  <br/> |
   
プログラムから、インデックスによって [ExtraInfo] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
| 行インデックス:  <br/> |**visRow1stHyperlink** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visHLinkExtraInfo** <br/> |
   

