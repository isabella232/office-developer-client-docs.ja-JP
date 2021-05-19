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
ms.openlocfilehash: d341acfbd47446a5b6dbee51ed821d1e1f34e15d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420179"
---
# <a name="label-cell-shape-data-section"></a>[Label] セル ([Shape Data] セクション)

[**図形データ**] ウィンドウに表示されるラベルを指定します。ラベルには、英数字とアンダースコア (_) 文字を使用できます。 
  
## <a name="remarks"></a>注釈

このセルではラベルの文字列が自動的に引用符で囲まれますが、[**図形データ**] ウィンドウでは引用符は表示されません。 
  
ラベル テキストがない場合、[**図形データ**] ウィンドウには行の名前 (Prop.Row) が表示されます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Label] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Prop. *Name*  .Prop のラベル。  *名前*  は行名です  <br/> |
   
プログラムから、インデックスによって [Label] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionProp** <br/> |
|行インデックス:  <br/> |**visRowProp**  +  *i* *=* 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visCustPropsLabel** <br/> |
   

