---
title: '[Overline] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251728
localization_priority: Normal
ms.assetid: 102cce17-43ee-e313-3412-a72d6ee18fe6
description: テキストの上に線を描画するかどうかを指定します。
ms.openlocfilehash: 3ceb0f5bcb6f66098938e49ea5f176921d0c9808
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805946"
---
# <a name="overline-cell-character-section"></a>[Overline] セル ([文字] セクション)

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
|セル名:  <br/> |Char.Overline [ *i* ]、 *i* = < 1 > 2 です。 3.  <br/> |
   
プログラムから、インデックスによって [Overline] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
|行インデックス:  <br/> |**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visCharacterOverline** <br/> |
   

