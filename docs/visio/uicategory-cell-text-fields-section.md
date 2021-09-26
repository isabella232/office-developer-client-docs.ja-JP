---
title: '[UICategory] セル ([Text Fields] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1070
ms.localizationpriority: medium
ms.assetid: 365f7005-ba34-2311-4c5c-16344962fc3f
description: Visio 2000 よりも前のバージョンの Visio に挿入するフィールドのカテゴリを指定します。
ms.openlocfilehash: c7733b73338fabee3759169cce9374f8d56bbf1e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627222"
---
# <a name="uicategory-cell-text-fields-section"></a>[UICategory] セル ([Text Fields] セクション)

Visio 2000 よりも前のバージョンの Visio に挿入するフィールドのカテゴリを指定します。
  
## <a name="remarks"></a>注釈

このセルは [シェイプシート] ウィンドウには表示されません。Visio バージョン 2000 の図面を Visio Version 5.0 ファイル形式で保存するなど、下位互換性の問題に対処する必要がある場合に、このセルを使用します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [UICategory] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Fields.UICat[  *i*  ] ここで  *、i*  = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [UICategory] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionTextField** <br/> |
| 行インデックス:  <br/> |**visRowField**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visFieldUICategory** <br/> |
   

