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
ms.openlocfilehash: ea747620301a07cafaf179106b54510edb95f7ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314799"
---
# <a name="size-cell-character-section"></a>[Size] セル ([Character] セクション)

図形のテキスト ブロックにあるテキストのサイズを指定します。
  
## <a name="remarks"></a>解説

テキストのサイズは図面の縮尺による影響を受けません。図面の縮尺を変更しても、テキストのサイズは変わりません。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Size] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Char. Size [ *i* ] = ** <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Size] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス :  <br/> |**visSectionCharacter** <br/> |
| 行インデックス:  <br/> |**visRowCharacter** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス :  <br/> |**visCharacterSize** <br/> |
   

