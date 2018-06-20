---
title: '[OutputFormat] セル ([Document Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251617
localization_priority: Normal
ms.assetid: 17238019-c800-5d3a-32f6-fb0008d4e25f
description: 図面の出力形式を指定します。図面ページは、通常は印刷用に形式が設定されていますが (既定値)、他の出力形式を選択することもできます。
ms.openlocfilehash: 7103fa5c2bc721add3496b7a497989d6632d58f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805944"
---
# <a name="outputformat-cell-document-properties-section"></a>[OutputFormat] セル ([Document Properties] セクション)

図面の出力形式を指定します。図面ページは、通常は印刷用に形式が設定されていますが (既定値)、他の出力形式を選択することもできます。
  
|**値**|**出力形式**|
|:-----|:-----|
| 0  <br/> | 印刷 (既定値)  <br/> |
| 1  <br/> | PowerPoint スライド ショー  <br/> |
| 2  <br/> | HTML または GIF 出力  <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって OutputFormat] セルへの参照を取得するには、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | そうです。  <br/> |
   
プログラムから、インデックスによって [OutputFormat] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowDoc** <br/> |
| セル インデックス:  <br/> |**visDocOutputFormat** <br/> |
   

