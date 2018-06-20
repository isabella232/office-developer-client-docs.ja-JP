---
title: '[X Dynamics] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1145
localization_priority: Normal
ms.assetid: 9757dfb4-6d37-0517-17fe-7593ff12bbfe
description: X を表す-ローカル座標でのコントロール ハンドルのアンカー ポイントの座標です。
ms.openlocfilehash: 9dee2381c15ed2817df9f89ebc830cf31bf64c1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806834"
---
# <a name="x-dynamics-cell-controls-section"></a>[X Dynamics] セル ([Controls] セクション)

*X*を表す-ローカル座標でのコントロール ハンドルのアンカー ポイントの座標です。 
  
## <a name="remarks"></a>備考

アンカー ポイントは、ダイナミックス機能を使うときのラバーバンディングに使用されます。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[X Dynamics] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | 制御します。  *名*です。XDynwhere を制御します。  *名*は、コントロールの行の名前です。  <br/> |
   
プログラムから、インデックスによって [X Dynamics] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionControls** <br/> |
| 行インデックス:  <br/> |**visRowControl** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visCtlXDyn** <br/> |
   

