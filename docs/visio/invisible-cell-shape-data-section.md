---
title: '[Invisible] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251341
localization_priority: Normal
ms.assetid: 5f368c2e-2a40-38ee-3568-ed5c57633345
description: '[図形データ] ウィンドウに、図形データ項目を表示するかどうかを指定します。'
ms.openlocfilehash: 8671fcc249b7ca81c011f697721093e7842c1558
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357268"
---
# <a name="invisible-cell-shape-data-section"></a>[Invisible] セル ([Shape Data] セクション)

[**図形データ**] ウィンドウに、図形データ項目を表示するかどうかを指定します。 
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形データ項目を表示しません。  <br/> |
| FALSE  <br/> | 図形データ項目を表示します。  <br/> |
   
## <a name="remarks"></a>解説

このセルの値は、[**図形データの定義**] ダイアログ ボックスの [**表示しない**] チェック ボックスに対応しています (このダイアログ ボックスを開くには、図形を右クリックし、[**データ**] をポイントして、[**図形データの定義**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Invisible] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | 提案. *名前*です。Prop の場合は非表示です。 *name*には、行の名前を指定します。  <br/> |
   
プログラムから、インデックスによって [Invisible] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionProp** <br/> |
| 行インデックス:  <br/> |**visRowProp** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visCustPropsInvis** <br/> |
   

