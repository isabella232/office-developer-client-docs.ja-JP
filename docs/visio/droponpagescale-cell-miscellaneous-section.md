---
title: '[DropOnPageScale] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60042
ms.localizationpriority: medium
ms.assetid: 8927f811-7d8e-ed54-9eec-b86a781168dd
ms.openlocfilehash: d8dad81ea4f20bfc78434e2439dfa70932cc7390
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594546"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a>[DropOnPageScale] セル ([Miscellaneous] セクション)

図形を図面ページにドロップしたときの縮尺のパーセント値が含まれます。
  
## <a name="remarks"></a>注釈

次の 2 つの場合に Visio は図形を図面ページで適切に表示されるよう縮尺します。
  
- 縮尺図面に未測定図形をドロップしたとき。
    
- 測定された図形がスケールされていない図面にドロップされる場合。
    
[DropOnPageScale] セルのパーセンテージは、図形Visio \> (100) または下 ( 100) のスケールの係数を \< 示します。 ハードコードされた値を計算する場合に、この数字を係数に使用することができます。 
  
縮尺図面の測定済み図形または非縮尺図面の未測定図形では、この値は 100% です。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DropOnPageScale] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | DropOnPageScale  <br/> |
   
プログラムから、インデックスによって [DropOnPageScale] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowMisc** <br/> |
| セル インデックス:  <br/> |**visObjDropOnPageScale** <br/> |
   

