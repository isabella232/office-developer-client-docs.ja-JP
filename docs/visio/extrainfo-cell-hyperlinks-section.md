---
title: '[ExtraInfo] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm360
ms.localizationpriority: medium
ms.assetid: 55834445-8619-f79a-aea0-0f6a1780e016
description: イメージ マップの座標など、URL の解決に使用される情報を渡す文字列を表します。 たとえば、[ExtraInfo] セルで、x=41 &amp; y=7 はイメージ マップの座標を指定します。
ms.openlocfilehash: 1b913c549bf11d999afb0866b9927fa5fa270be3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570653"
---
# <a name="extrainfo-cell-hyperlinks-section"></a>[ExtraInfo] セル ([Hyperlinks] セクション)

イメージ マップの座標など、URL の解決に使用される情報を渡す文字列を表します。 たとえば、[ExtraInfo] セルの "x=41 y=7" はイメージ マップの座標 &amp; を指定します。
  
## <a name="remarks"></a>注釈

イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ExtraInfo] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ハイパーリンク  *name*  .ExtraInfo where Hyperlink.  *name*  は行名です  <br/> |
   
プログラムから、インデックスによって [ExtraInfo] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
| 行インデックス:  <br/> |**visRow1stHyperlink**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visHLinkExtraInfo** <br/> |
   

