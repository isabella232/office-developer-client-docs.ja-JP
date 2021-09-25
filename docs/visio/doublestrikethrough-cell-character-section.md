---
title: '[DoubleStrikethrough] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033762
ms.localizationpriority: medium
ms.assetid: c48a77e1-ea3c-7a6d-8c05-f9e0cb434cda
description: テキストを二重取り消し線で書式設定するかどうかを指定します。
ms.openlocfilehash: 0589acb6dcec0664c749f1b48af4a0b3e67db177
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590276"
---
# <a name="doublestrikethrough-cell-character-section"></a>[DoubleStrikethrough] セル ([Character] セクション)

テキストを二重取り消し線で書式設定するかどうかを指定します。
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DoubleStrikethrough] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Char.DoubleStrikethrough[ i ]*ここで**、i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [DoubleStrikethrough] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
| 行インデックス:  <br/> |**visRowCharacter**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visCharacterDoubleStrikethrough** <br/> |
   

