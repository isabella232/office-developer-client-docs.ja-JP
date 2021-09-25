---
title: '[BeginArrow] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51105
ms.localizationpriority: medium
ms.assetid: 0ab4044e-2d77-1fbe-ef20-5d029bc064ba
description: 線の最初の頂点に対して、矢印を付けるか、または別の書式の端点を適用するかを指定します。0 ～ 45 の数値を入力するか、またはユーザーが設定した線の端点名を使用して USE 関数を入力します。[線] ダイアログ ボックスを使用することもできます。
ms.openlocfilehash: 9ad6aa363e54f9c11b6f5c9fc9b38ab52d6cb7a9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554923"
---
# <a name="beginarrow-cell-line-format-section"></a>[BeginArrow] セル ([Line Format] セクション)

線の最初の頂点に対して、矢印を付けるか、または別の書式の端点を適用するかを指定します。0 ～ 45 の数値を入力するか、またはユーザーが設定した線の端点名を使用して USE 関数を入力します。**[線]** ダイアログ ボックスを使用することもできます。 
  
|**値**|**説明**|
|:-----|:-----|
| 0  <br/> | 矢印を付けません。  <br/> |
| 1 ～ 45  <br/> | さまざまな矢印のスタイル。入力した値は、[**線**] ダイアログ ボックスでインデックスが付けられたエントリに対応します。  <br/> |
   
## <a name="remarks"></a>注釈

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
   

