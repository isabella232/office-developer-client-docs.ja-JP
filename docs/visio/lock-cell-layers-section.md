---
title: '[Lock] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm590
ms.localizationpriority: medium
ms.assetid: 47bb268f-acdd-7369-716c-bd51a32b8a49
description: レイヤーに属する図形に対する選択操作や編集操作をロックするかどうかを指定します。
ms.openlocfilehash: 62ae9a41a2ba38b35469026525a6549cd72ba467
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612506"
---
# <a name="lock-cell-layers-section"></a>[Lock] セル ([Layers] セクション)

レイヤーに属する図形に対する選択操作や編集操作をロックするかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |図形をロックします。  <br/> |
|FALSE  <br/> |図形をロックしません。  <br/> |
   
## <a name="remarks"></a>注釈

この値は、[**レイヤー プロパティ**] ダイアログ ボックスの [**ロック**] を選択して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**編集**] グループで、[**レイヤー**] をクリックして、[**レイヤー プロパティ**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Lock] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Layers.Locked[ *i*  ] ここで  *、i*  = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Lock] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionLayer** <br/> |
|行インデックス:  <br/> |**visRowLayer**  +  *i* *=* 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visLayerLock** <br/> |
   

