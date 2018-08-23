---
title: '[BeginArrow] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51105
localization_priority: Normal
ms.assetid: 0ab4044e-2d77-1fbe-ef20-5d029bc064ba
description: 線の最初の頂点に対して、矢印を付けるか、または別の書式の端点を適用するかを指定します。0 ～ 45 の数値を入力するか、またはユーザーが設定した線の端点名を使用して USE 関数を入力します。[線] ダイアログ ボックスを使用することもできます。
ms.openlocfilehash: c6d5a66d76cfea61b1c9923c5b904dadec5495f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804795"
---
# <a name="beginarrow-cell-line-format-section"></a>[BeginArrow] セル ([線の書式設定] セクション)

線の最初の頂点に対して、矢印を付けるか、または別の書式の端点を適用するかを指定します。0 ～ 45 の数値を入力するか、またはユーザーが設定した線の端点名を使用して USE 関数を入力します。**[線]** ダイアログ ボックスを使用することもできます。 
  
|**値**|**説明**|
|:-----|:-----|
| 0  <br/> | 矢印を付けません。  <br/> |
| 1-45  <br/> | さまざまな矢印のスタイル。入力した値は、[**線**] ダイアログ ボックスでインデックスが付けられたエントリに対応します。  <br/> |
   
## <a name="remarks"></a>備考

矢印のサイズは [BeginArrowSize] セルで設定します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BeginArrow] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | BeginArrow  <br/> |
   
プログラムから、インデックスによって [BeginArrow] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLine** <br/> |
| セル インデックス:  <br/> |**visLineBeginArrow** <br/> |
   

