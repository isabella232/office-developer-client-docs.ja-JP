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
description: '[図形データ] ウィンドウ内の項目が表示されている順序に影響を与える文字列と評価されます。'
ms.openlocfilehash: 1dbc093f2cee509531b8148563fbdb1a777a349f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806551"
---
# <a name="sortkey-cell-shape-data-section"></a>[SortKey] セル ([Shape Data] セクション)

[**図形データ**] ウィンドウ内の項目が表示されている順序に影響を与える文字列と評価されます。 
  
## <a name="remarks"></a>備考

[Sortkey] の値を比較するために使用する計算は、およびロケール固有の大文字小文字を区別します。 [Sortkey] の値が等しい場合は、図形データ行の順序が表示されます。 並べ替えキーが図形データは、並べ替えキーが含まれている図形データの後に一覧表示されません。
  
次の順序で、[**図形データ**] ウィンドウで図形データを表示するのには並べ替えキーを使用する場合の例: 品目番号、数量、価格です。 
  
 *行ラベル、* および *[sortkey]* は、図形データ行のセルを参照してください。 この例では、図形データ行に名前が付いています。 
  
|**Row**|**Label**|**[Sortkey]**|
|:-----|:-----|:-----|
| Prop.Item  <br/> | 項目番号  <br/> | 1  <br/> |
| 付ける  <br/> | 価格  <br/> | 3  <br/> |
| Prop.Quan  <br/> | 数量  <br/> | 2  <br/> |
   
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [sortkey] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | プロペラです。 *名*です。[Sortkey] プロパティでは。 *名前*は、カスタム プロパティ行の名前  <br/> |
   
プログラムから、インデックスによって [sortkey] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionProp** <br/> |
| 行インデックス:  <br/> |**visRowProp** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visCustPropsSortKey** <br/> |
   

