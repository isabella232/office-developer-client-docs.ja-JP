---
title: '[Strikethru] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm975
ms.localizationpriority: medium
ms.assetid: b03b4415-0b1a-eb03-2b5e-373b39a0f07a
description: テキストを取り消し線として書式設定するかどうかを指定します。
ms.openlocfilehash: 0f1f997fe79e365e7dd60dd48c4b889a78d96b97
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549491"
---
# <a name="strikethru-cell-character-section"></a>[Strikethru] セル ([Character] セクション)

テキストを取り消し線として書式設定するかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |テキストを取り消し線として書式設定します。  <br/> |
|FALSE  <br/> |テキストを取り消し線として書式設定しません。  <br/> |
   
## <a name="remarks"></a>注釈

このセルの値は、[**テキスト**] ダイアログ ボックスを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブで [**フォント**] 矢印をクリックします)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Strikethru] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Char.Strikethru[ i ]*ここで**、i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Strikethru] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
|行インデックス:  <br/> |**visRowCharacter**  +  *i* *=* 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visCharacterStrikethru** <br/> |
   

