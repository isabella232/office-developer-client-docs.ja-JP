---
title: '[UICode] セル ([Text Fields] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1075
localization_priority: Normal
ms.assetid: 1d9717c1-4310-0d62-874f-4df77cd81627
description: Visio 2000 よりも前のバージョンの Visio に挿入するフィールドのコードを指定します。
ms.openlocfilehash: ce05f779bfebd5720555f1a2d92b1f9f92cfbdfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806717"
---
# <a name="uicode-cell-text-fields-section"></a>[UICode] セル ([Text Fields] セクション)

Visio 2000 よりも前のバージョンの Visio に挿入するフィールドのコードを指定します。
  
## <a name="remarks"></a>備考

このセルは [シェイプシート] ウィンドウには表示されません。Visio バージョン 2000 の図面を Visio Version 5.0 ファイル形式で保存するなど、下位互換性の問題に対処する必要がある場合に、このセルを使用します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [uicode] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Fields.UICod [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [uicode] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionTextField** <br/> |
| 行インデックス:  <br/> |**visRowField** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visFieldUICode** <br/> |
   

