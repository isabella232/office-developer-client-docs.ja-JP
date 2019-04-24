---
title: '[UIFormat] セル ([Text Fields] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1080
localization_priority: Normal
ms.assetid: 0dddef20-c58e-2306-ab8e-6cac8e159f61
description: Visio 2000 よりも前のバージョンの Visio に挿入するフィールドの書式を指定します。
ms.openlocfilehash: 16cefc5f45d6b5f0f677e35bd5d0937d48fb2680
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337143"
---
# <a name="uiformat-cell-text-fields-section"></a>[UIFormat] セル ([Text Fields] セクション)

Visio 2000 よりも前のバージョンの Visio に挿入するフィールドの書式を指定します。
  
## <a name="remarks"></a>解説

このセルは [シェイプシート] ウィンドウには表示されません。Visio バージョン 2000 の図面を Visio Version 5.0 ファイル形式で保存するなど、下位互換性の問題に対処する必要がある場合に、このセルを使用します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [UIFormat] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | フィールド uifmt [ *i* ]。 *i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [UIFormat] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionTextField** <br/> |
| 行インデックス:  <br/> |**visRowField** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visFieldUIFormat** <br/> |
   

