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
ms.openlocfilehash: 137d22430829f96a9c6ad69a73a6b44e964d5f4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355896"
---
# <a name="value-cell-user-defined-cells-section"></a>[Value] セル ([User-Defined Cells] セクション)

対応するユーザー定義のセルの値を指定します。
  
## <a name="remarks"></a>解説

別のセルでこの値を参照するには、行ラベル [User.Row] に入力したユーザー定義の名前を指定します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Value] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | マニュアル.  *名前*です。Value (ユーザーの場合)。  *name*には、行の名前を指定します。  <br/> |
   
プログラムから、インデックスによって [Value] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionUser** <br/> |
| 行インデックス:  <br/> |**visRowUser** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visUserValue** <br/> |
   

