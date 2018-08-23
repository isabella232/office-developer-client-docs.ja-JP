---
title: '[DropOnPageScale] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60042
localization_priority: Normal
ms.assetid: 8927f811-7d8e-ed54-9eec-b86a781168dd
ms.openlocfilehash: a586cca497e1ba04848142917a84c3aa8a25d081
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805272"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a>[DropOnPageScale] セル ([その他] セクション)

図形を図面ページにドロップしたときの縮尺のパーセント値が含まれます。
  
## <a name="remarks"></a>備考

次の 2 つの場合に Visio は図形を図面ページで適切に表示されるよう縮尺します。
  
- 縮尺図面に未測定図形をドロップしたとき。
    
- 非縮尺図面に測定済み図形をドロップしたとき。
    
DropOnPageScale] セルの割合が、縮小される因数を Visio 図形のいずれかの方法を示します (\>100)、下 (\<100)。 係数としてこの番号を使用するには、ハード コーディングされた値を計算するときです。 
  
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
   

