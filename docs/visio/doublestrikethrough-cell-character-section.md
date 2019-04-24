---
title: '[DoubleStrikethrough] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033762
localization_priority: Normal
ms.assetid: c48a77e1-ea3c-7a6d-8c05-f9e0cb434cda
description: テキストを二重取り消し線で書式設定するかどうかを指定します。
ms.openlocfilehash: d8ef5bdb6e086be9657f51c66c10d578414e1deb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360593"
---
# <a name="doublestrikethrough-cell-character-section"></a>[DoubleStrikethrough] セル ([Character] セクション)

テキストを二重取り消し線で書式設定するかどうかを指定します。
  
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DoubleStrikethrough] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [doublestrikethrough] [ *i* ] *i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [DoubleStrikethrough] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
| 行インデックス:  <br/> |**visRowCharacter** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visCharacterDoubleStrikethrough** <br/> |
   

