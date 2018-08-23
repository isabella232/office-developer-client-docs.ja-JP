---
title: '[Label] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm510
localization_priority: Normal
ms.assetid: 6d328b1c-8d92-eb1a-7317-7dd85c674ff9
description: '[図形データ] ウィンドウに表示されるラベルを指定します。ラベルには、英数字とアンダースコア (_) 文字を使用できます。'
ms.openlocfilehash: 087bcb87a9e47131e6dbcd2d8df5c5da8a06894b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805634"
---
# <a name="label-cell-shape-data-section"></a>[Label] セル ([図形データ] セクション)

[**図形データ**] ウィンドウに表示されるラベルを指定します。ラベルには、英数字とアンダースコア (_) 文字を使用できます。 
  
## <a name="remarks"></a>注釈

このセルではラベルの文字列が自動的に引用符で囲まれますが、[**図形データ**] ウィンドウでは引用符は表示されません。 
  
ラベル テキストがない場合、[**図形データ**] ウィンドウには行の名前 (Prop.Row) が表示されます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Label] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |プロペラです。*名*です。ラベル位置プロパティです。 *名前*は、行の名前  <br/> |
   
プログラムから、インデックスによって [Label] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionProp** <br/> |
|行インデックス:  <br/> |**visRowProp** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visCustPropsLabel** <br/> |
   

