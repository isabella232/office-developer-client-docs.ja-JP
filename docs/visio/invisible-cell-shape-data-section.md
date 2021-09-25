---
title: '[Invisible] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251341
ms.localizationpriority: medium
ms.assetid: 5f368c2e-2a40-38ee-3568-ed5c57633345
description: '[図形データ] ウィンドウに、図形データ項目を表示するかどうかを指定します。'
ms.openlocfilehash: 046ae26940da77297b1671af29ace286314dd730
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582618"
---
# <a name="invisible-cell-shape-data-section"></a>[Invisible] セル ([Shape Data] セクション)

[**図形データ**] ウィンドウに、図形データ項目を表示するかどうかを指定します。 
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形データ項目を表示しません。  <br/> |
| FALSE  <br/> | 図形データ項目を表示します。  <br/> |
   
## <a name="remarks"></a>注釈

このセルの値は、[**図形データの定義**] ダイアログ ボックスの [**表示しない**] チェック ボックスに対応しています (このダイアログ ボックスを開くには、図形を右クリックし、[**データ**] をポイントして、[**図形データの定義**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Invisible] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Prop。  *name*  .Prop の場所を非表示にします。  *name*  は行名です  <br/> |
   
プログラムから、インデックスによって [Invisible] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionProp** <br/> |
| 行インデックス:  <br/> |**visRowProp**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visCustPropsInvis** <br/> |
   

