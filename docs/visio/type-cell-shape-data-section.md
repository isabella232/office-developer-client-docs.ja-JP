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
ms.openlocfilehash: e5471dcc1ed487a5992779f1faa4763887bebb2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806704"
---
# <a name="type-cell-shape-data-section"></a>[Type] セル ([Shape Data] セクション)

図形データ値のデータの種類を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |文字列。これは既定値です。  <br/> |**visPropTypeString** <br/> |
|1  <br/> |固定リスト。 **図形データの定義**] ダイアログ ボックスの一覧の項目のドロップダウン コンボ ボックスを表示します。 Format] セルに、リスト項目を指定します。 ユーザーは、一覧から 1 項目だけを選択できます。  <br/> |**visPropTypeListFix** <br/> |
|2  <br/> |数値。日付、時刻、期間、通貨の値の他、スカラー、寸法、角度も含まれます。書式形式は [Format] セルで指定します。  <br/> |**visPropTypeNumber** <br/> |
|3  <br/> |ブール値です。 FALSE および true を指定するように、[**図形データの定義**] ダイアログ ボックス内のドロップ ダウン リスト ボックスから選択できる項目を表示します。  <br/> |**visPropTypeBool** <br/> |
|4  <br/> |変数の一覧です。 **図形データの定義**] ダイアログ ボックスの一覧の項目のドロップダウン コンボ ボックスを表示します。 Format] セルに、リスト項目を指定します。 ユーザーでは、リスト項目を選択したり、セルの書式での現在のリストに追加される新しい項目を入力することができます。  <br/> |**visPropTypeListVar** <br/> |
|5  <br/> |日付または時刻の値。日、月、年、および秒、分、時間、または日付と時刻の組み合わせを表示します。書式形式は [Format] セルで指定します。  <br/> |**visPropTypeDate** <br/> |
|6  <br/> |期間の値。経過時間を表示します。書式形式は [Format] セルで指定します。  <br/> |**visPropTypeDuration** <br/> |
|7  <br/> |通貨の値。システムに適用されている現在の地域別設定を使用します。書式形式は [Format] セルで指定します。  <br/> |**visPropTypeCurrency** <br/> |
   
## <a name="remarks"></a>備考

取得する、[Type] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |プロペラです。*名*です。型、プロペラします。 *名前*は、行の名前  <br/> |
   
プログラムから、インデックスによって [Type] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionProp** <br/> |
|行インデックス:  <br/> |**visRowProp** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visCustPropsType** <br/> |
   
