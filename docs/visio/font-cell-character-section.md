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
ms.openlocfilehash: cbbf2a2400c995e0cbc217c1161fbd18f7459b28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805410"
---
# <a name="font-cell-character-section"></a>[Font] セル ([文字] セクション)

テキストの書式設定に使用するフォントの番号を表します。フォント番号は、システムにインストールされたフォントによって異なります。フォント番号は既定のフォントを示し、通常はＭＳ Ｐゴシックです。
  
## <a name="remarks"></a>備考

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Font] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Char.Font [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [Font] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
| 行インデックス:  <br/> |**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visCharacterFont** <br/> |
   

