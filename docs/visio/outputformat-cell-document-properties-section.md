---
title: '[OutputFormat] セル ([Document Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251617
ms.localizationpriority: medium
ms.assetid: 17238019-c800-5d3a-32f6-fb0008d4e25f
description: 図面の出力形式を指定します。図面ページは、通常は印刷用に形式が設定されていますが (既定値)、他の出力形式を選択することもできます。
ms.openlocfilehash: b4e2c63912509c9cdae04f828e138ef90fbe4859
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577816"
---
# <a name="outputformat-cell-document-properties-section"></a>[OutputFormat] セル ([Document Properties] セクション)

図面の出力形式を指定します。図面ページは、通常は印刷用に形式が設定されていますが (既定値)、他の出力形式を選択することもできます。
  
|**値**|**出力形式**|
|:-----|:-----|
| 0  <br/> | 印刷 (既定値)  <br/> |
| 1  <br/> | PowerPoint スライド ショー  <br/> |
| 2  <br/> | HTML または GIF 出力  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [OutputFormat] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | OutputFormat  <br/> |
   
プログラムから、インデックスによって [OutputFormat] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowDoc** <br/> |
| セル インデックス:  <br/> |**visDocOutputFormat** <br/> |
   

