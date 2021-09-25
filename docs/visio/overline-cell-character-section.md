---
title: '[Overline] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251728
ms.localizationpriority: medium
ms.assetid: 102cce17-43ee-e313-3412-a72d6ee18fe6
description: テキストの上に線を描画するかどうかを指定します。
ms.openlocfilehash: 4cf5c75f15fd9e40f5c59c9ff679de3de1dd9ae9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623314"
---
# <a name="overline-cell-character-section"></a>[Overline] セル ([Character] セクション)

テキストの上に線を描画するかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |テキストの上に線を描画します。  <br/> |
|FALSE  <br/> |テキストの上に線を描画しません。  <br/> |
   
## <a name="remarks"></a>注釈

このセルの値は、[**テキスト**] ダイアログ ボックスを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブで [**フォント**] 矢印をクリックします)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Overline] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Char.Overline[ *i*  ]  *ここで、i*  = <1>、2. 3...  <br/> |
   
プログラムから、インデックスによって [Overline] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
|行インデックス:  <br/> |**visRowCharacter**  +  *i* *=* 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visCharacterOverline** <br/> |
   

