---
title: '[Font] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm390
localization_priority: Normal
ms.assetid: 935760a9-307e-90bc-c301-d04283d97427
description: テキストの書式設定に使用するフォントの番号を表します。フォント番号は、システムにインストールされたフォントによって異なります。フォント番号は既定のフォントを示し、通常はＭＳ Ｐゴシックです。
ms.openlocfilehash: d9182932b8fa63c30473b93e420aa9efe30bf5eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438667"
---
# <a name="font-cell-character-section"></a>[Font] セル ([Character] セクション)

テキストの書式設定に使用するフォントの番号を表します。フォント番号は、システムにインストールされたフォントによって異なります。フォント番号は既定のフォントを示し、通常はＭＳ Ｐゴシックです。
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Font] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Char フォント [ *i* ] = <1> ** 、2、3...  <br/> |
   
プログラムから、インデックスによって [Font] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
| 行インデックス:  <br/> |**visRowCharacter** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visCharacterFont** <br/> |
   

