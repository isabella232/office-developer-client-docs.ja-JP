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
description: イメージ マップの座標など、URL の解決に使用される情報を渡す文字列を表します。 たとえば、[ExtraInfo] セルの x = 41&amp;y = 7specifies、イメージマップの座標を指定します。
ms.openlocfilehash: df2886ef7911b484cc60e8a476bfa53369fbf646
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357821"
---
# <a name="extrainfo-cell-hyperlinks-section"></a>[ExtraInfo] セル ([Hyperlinks] セクション)

イメージ マップの座標など、URL の解決に使用される情報を渡す文字列を表します。 たとえば、[ExtraInfo] セルの "x = 41&amp;y = 7" では、イメージマップの座標を指定します。
  
## <a name="remarks"></a>解説

イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ExtraInfo] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ハイパーリンク  *名前*です。引数 ExtraInfo のハイパーリンクを指定します。  *name*には、行の名前を指定します。  <br/> |
   
プログラムから、インデックスによって [ExtraInfo] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
| 行インデックス:  <br/> |**visRow1stHyperlink** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**vishlinkextrainfo** <br/> |
   

