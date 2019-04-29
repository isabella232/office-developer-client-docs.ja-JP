---
title: '[SortKey] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251345
localization_priority: Normal
ms.assetid: 67fa5389-f0b9-a9db-8d19-9b16e256dfa3
description: このセルの値は文字列として扱われ、評価されます。この値に基づいて、[図形データ] ウィンドウ内にある項目を一覧表示するための順序が決まります。
ms.openlocfilehash: d166ea18a36f6a4101b8933fce804be2243954bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417855"
---
# <a name="sortkey-cell-shape-data-section"></a>[SortKey] セル ([Shape Data] セクション)

このセルの値は文字列として扱われ、評価されます。この値に基づいて、[**図形データ**] ウィンドウ内にある項目を一覧表示するための順序が決まります。 
  
## <a name="remarks"></a>注釈

[SortKey] の値を比較するときに使用される計算方法は、ロケールに固有のもので、大文字と小文字は区別されます。 [SortKey] の値が等しい場合は、図形データは行の順序に基づいて一覧表示されます。 並べ替えキーを持たない図形データは、並べ替えキーを含む図形データの後に表示されます。
  
並べ替えキーを使用して、[**図形データ**] ウィンドウに、項目番号、数量、および価格の順序で図形データを表示する例を次に示します。 
  
 *行、ラベル、* および*SortKey*は、図形データ行のセルを参照します。 この例では、図形データ行に名前が付けられています。 
  
|**Row**|**Label**|**[sortkey]**|
|:-----|:-----|:-----|
| Prop. アイテム  <br/> | 項目番号  <br/> | 1   <br/> |
| Prop  <br/> | Price  <br/> | 3   <br/> |
| Prop  <br/> | 数量  <br/> | 2   <br/> |
   
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [SortKey] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | 提案. *名前*です。SortKey (Prop) *name*はカスタムプロパティ行の名前です。  <br/> |
   
プログラムから、インデックスによって [SortKey] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionProp** <br/> |
| 行インデックス:  <br/> |**visRowProp** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**viscustpropssortkey** <br/> |
   

