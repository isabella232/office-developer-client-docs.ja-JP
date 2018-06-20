---
title: '[Size] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251252
localization_priority: Normal
ms.assetid: a61b50fe-eacb-b3d4-0e4e-ab3e7c972ee9
description: 図形のテキスト ブロックにあるテキストのサイズを指定します。
ms.openlocfilehash: f3077441844b859cf224eccc8180d0d56cce851f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806497"
---
# <a name="size-cell-character-section"></a>[Size] セル ([Character] セクション)

図形のテキスト ブロックにあるテキストのサイズを指定します。
  
## <a name="remarks"></a>備考

テキストのサイズは図面の縮尺による影響を受けません。図面の縮尺を変更しても、テキストのサイズは変わりません。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Size] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Char.Size [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [Size] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
| 行インデックス:  <br/> |**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visCharacterSize** <br/> |
   

