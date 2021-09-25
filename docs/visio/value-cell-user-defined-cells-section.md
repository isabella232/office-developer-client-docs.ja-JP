---
title: '[Value] セル ([User-Defined Cells] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1100
ms.localizationpriority: medium
ms.assetid: 495b2aec-e197-75eb-9974-e7c92d26546f
description: 対応するユーザー定義のセルの値を指定します。
ms.openlocfilehash: 00a96f98682ace7c66ddba8c7aa7ac3a284a224c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559347"
---
# <a name="value-cell-user-defined-cells-section"></a>[Value] セル ([User-Defined Cells] セクション)

対応するユーザー定義のセルの値を指定します。
  
## <a name="remarks"></a>注釈

別のセルでこの値を参照するには、行ラベル [User.Row] に入力したユーザー定義の名前を指定します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Value] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | ユーザー。  *Name*  .ユーザーの値。  *名前*  は行名です  <br/> |
   
プログラムから、インデックスによって [Value] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionUser** <br/> |
| 行インデックス:  <br/> |**visRowUser**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visUserValue** <br/> |
   

