---
title: '[Font] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm390
ms.localizationpriority: medium
ms.assetid: 935760a9-307e-90bc-c301-d04283d97427
description: テキストの書式設定に使用するフォントの番号を表します。フォント番号は、システムにインストールされたフォントによって異なります。フォント番号は既定のフォントを示し、通常はＭＳ Ｐゴシックです。
ms.openlocfilehash: 2c85c979d2e08c44c9abd6797ca36252bc96199e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618932"
---
# <a name="font-cell-character-section"></a>[Font] セル ([Character] セクション)

テキストの書式設定に使用するフォントの番号を表します。フォント番号は、システムにインストールされたフォントによって異なります。フォント番号は既定のフォントを示し、通常はＭＳ Ｐゴシックです。
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Font] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Char.Font[  *i*  ] ここで  *、i*  = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Font] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
| 行インデックス:  <br/> |**visRowCharacter**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visCharacterFont** <br/> |
   

