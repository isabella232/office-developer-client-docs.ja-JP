---
title: '[Value] セル ([User-Defined Cells] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1100
localization_priority: Normal
ms.assetid: 495b2aec-e197-75eb-9974-e7c92d26546f
description: 対応するユーザー定義のセルの値を指定します。
ms.openlocfilehash: d320c35fa8ae65dd0b21a83ad2cf23dbb3af77f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806754"
---
# <a name="value-cell-user-defined-cells-section"></a>[Value] セル ([User-Defined Cells] セクション)

対応するユーザー定義のセルの値を指定します。
  
## <a name="remarks"></a>備考

別のセルでこの値を参照するには、行ラベル [User.Row] に入力したユーザー定義の名前を指定します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [値] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ユーザーです。  *名*です。値の場所のユーザーです。  *名前*は、行の名前  <br/> |
   
プログラムから、インデックスによって [Value] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionUser** <br/> |
| 行インデックス:  <br/> |**visRowUser** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visUserValue** <br/> |
   

