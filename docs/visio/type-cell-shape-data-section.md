---
title: '[Type] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1055
localization_priority: Normal
ms.assetid: 1e24a906-83ce-32d2-5d7b-ba6dd6eea2d3
description: 図形データ値のデータの種類を指定します。
ms.openlocfilehash: c2d38b521a8597a4582a4145ad808b0c0e26ff0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350898"
---
# <a name="type-cell-shape-data-section"></a>[Type] セル ([Shape Data] セクション)

図形データ値のデータの種類を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|.0  <br/> |文字列。これは既定値です。  <br/> |**visPropTypeString** <br/> |
|1-d  <br/> |固定リスト。[**図形データの定義**] ダイアログ ボックスのドロップダウン コンボ ボックスにリスト項目を表示します。リスト項目は [Format] セルで指定します。このリストからは 1 つの項目だけを選択できます。<br/> |**visPropTypeListFix** <br/> |
|pbm-2  <br/> |数値。日付、時刻、期間、通貨の値の他、スカラー、寸法、角度も含まれます。書式形式は [Format] セルで指定します。  <br/> |**visPropTypeNumber** <br/> |
|1/3  <br/> |ブール演算型。[**図形データの定義**] ダイアログ ボックスのドロップダウン リスト ボックスから選択できる項目として、FALSE および TRUE を表示します。<br/> |**visPropTypeBool** <br/> |
|2/4  <br/> |変数リスト。[**図形データの定義**] ダイアログ ボックスのドロップダウン コンボ ボックスにリスト項目を表示します。リスト項目は [Format] セルで指定します。リスト項目を選択することも、新しい項目を入力して [Format] セルの現在のリストに追加することもできます。<br/> |**visPropTypeListVar** <br/> |
|5  <br/> |日付または時刻の値。日、月、年、および秒、分、時間、または日付と時刻の組み合わせを表示します。書式形式は [Format] セルで指定します。  <br/> |**visPropTypeDate** <br/> |
|シックス  <br/> |期間の値。経過時間を表示します。書式形式は [Format] セルで指定します。  <br/> |**visPropTypeDuration** <br/> |
|7  <br/> |通貨の値。システムに適用されている現在の地域別設定を使用します。書式形式は [Format] セルで指定します。  <br/> |**visPropTypeCurrency** <br/> |
   
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Type] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |提案.*名前*です。Prop と入力します。 *name*には、行の名前を指定します。  <br/> |
   
プログラムから、インデックスによって [Type] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionProp** <br/> |
|行インデックス:  <br/> |**visRowProp** +  *i* = ** 0、1、2...  <br/> |
|セル インデックス:  <br/> |**viscustpropstype** <br/> |
   

