---
title: '[Format] セル ([Text Fields] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm400
localization_priority: Normal
ms.assetid: ab937a00-84c2-6c1c-9080-b7c95ead4f63
description: テキスト フィールドの書式を指定します。文字列、数値、日付/時刻、期間、または通貨を指定できます。
ms.openlocfilehash: 767b658a9431dfab23d2df9bcfa6c83b52f48d75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805441"
---
# <a name="format-cell-text-fields-section"></a>[Format] セル ([Text Fields] セクション)

テキスト フィールドの書式を指定します。文字列、数値、日付/時刻、期間、または通貨を指定できます。
  
## <a name="remarks"></a>備考

Type] セルの値が 0、2、5、6、または 7 の場合 (文字列、数値、日付または時刻、期間、または通貨、それぞれ)、データの種類に適した書式形式を指定します。 たとえば、番号 12.43 in」# # 4 UU」の図の書式設定が書式設定します。 12 2/4 インチです。 図の書式設定を指定する方法の詳細については、[書式形式について](about-format-pictures.md)を参照してください。
  
数値 ([Type] セル = 2) は寸法、スカラー、角度、日付、時刻、通貨を表現できます。入力した数値が常に日付、時刻、または通貨として評価されるようにするには、[Format] セルに、書式形式ではなく DATETIME 関数または CY 関数を使用します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Format] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Fields.Format [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [Format] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionTextField** <br/> |
| 行インデックス:  <br/> |**visRowField** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visFieldFormat** <br/> |
   

