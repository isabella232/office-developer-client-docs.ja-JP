---
title: '[Pos] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm805
ms.localizationpriority: medium
ms.assetid: c02186ce-6a20-fbe7-588d-d64c3ea4dec4
description: 基線に対する、図形のテキストの位置を指定します。
ms.openlocfilehash: bde906d82b7583e86f5e6d2f6bc4a4c14d792a28
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623188"
---
# <a name="pos-cell-character-section"></a>[Pos] セル ([Character] セクション)

基線に対する、図形のテキストの位置を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 標準の位置  <br/> |**visPosNormal** <br/> |
| 1  <br/> | Superscript  <br/> |**visPosSuper** <br/> |
| 2  <br/> | Subscript  <br/> |**visPosSub** <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Pos] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Char.Pos[  *i*  ] ここで  *、i*  = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Pos] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
| 行インデックス:  <br/> |**visRowCharacter**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visCharacterPos** <br/> |
   

