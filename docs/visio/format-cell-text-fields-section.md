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
ms.openlocfilehash: c1c7fc7e9c699b7642369fbb979c005829b06cb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346019"
---
# <a name="format-cell-text-fields-section"></a>[Format] セル ([Text Fields] セクション)

テキスト フィールドの書式を指定します。文字列、数値、日付/時刻、期間、または通貨を指定できます。
  
## <a name="remarks"></a>解説

[Type] セルの値が 0、2、5、6、7 (文字列、数値、日付/時刻、期間、通貨を表します) の場合は、それぞれのデータの種類に適した書式形式を指定します。たとえば、"# #/4 UU" という書式形式では、「12.43 in」という数値を指定すると "12 2/4 インチ" と表示されます。書式形式の指定の詳細については、「[書式形式について](about-format-pictures.md)」を参照してください。
  
数値 ([Type] セル = 2) は寸法、スカラー、角度、日付、時刻、通貨を表現できます。入力した数値が常に日付、時刻、または通貨として評価されるようにするには、[Format] セルに、書式形式ではなく DATETIME 関数または CY 関数を使用します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Format] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | フィールドの形式 [ *i* ] = ** <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Format] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionTextField** <br/> |
| 行インデックス:  <br/> |**visRowField** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visFieldFormat** <br/> |
   

