---
title: '[DoubleULine] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm260
ms.localizationpriority: medium
ms.assetid: c18955c8-d653-c29d-d3da-9d3cd0241e17
description: テキストの範囲に二重下線を付けるかどうかを指定します。
ms.openlocfilehash: df544c67163e1c0894763ca227c5063133dc822f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628424"
---
# <a name="doubleuline-cell-character-section"></a>[DoubleULine] セル ([Character] セクション)

テキストの範囲に二重下線を付けるかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |テキストに二重下線を付けます。  <br/> |
|FALSE  <br/> |テキストに二重下線を付けません。  <br/> |
   
## <a name="remarks"></a>注釈

[Character] セクションに行が複数存在する場合、[DoubleULine] セルには図形のテキストのサブ範囲に適用される書式設定情報が表示されます。複数の行が含まれない場合は、このセルには、すべての図形のテキストに対する書式設定情報が表示されます。
  
このセルの値は、[**テキスト**] ダイアログ ボックスを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**フォント**] 矢印をクリックします)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DoubleULine] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Char.DblUnderline[ *i*  ]  *ここで、i*  = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [DoubleULine] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
|行インデックス:  <br/> |**visRowCharacter**  +  *i* *=* 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visCharacterDblUnderline** <br/> |
   

