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
description: 線の最初の頂点に、矢印またはその他の線の端点の書式があるかどうかを示します。 0 ~ 45 の数値、またはユーザー設定の線の端点の名前を使用する関数を入力するか、[線] ダイアログボックスを使用します。
ms.openlocfilehash: cf5a512dabd0e6296b83fa7bfd2a2a6134143d50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410295"
---
# <a name="beginarrow-cell-line-format-section"></a>[BeginArrow] セル ([Line Format] セクション)

線の最初の頂点に対して、矢印を付けるか、または別の書式の端点を適用するかを指定します。0 ～ 45 の数値を入力するか、またはユーザーが設定した線の端点名を使用して USE 関数を入力します。**[線]** ダイアログ ボックスを使用することもできます。 
  
|**値**|**説明**|
|:-----|:-----|
| .0  <br/> | 矢印を付けません。  <br/> |
| 1 ～ 45  <br/> | さまざまな矢印のスタイル。入力した値は、[**線**] ダイアログ ボックスでインデックスが付けられたエントリに対応します。  <br/> |
   
## <a name="remarks"></a>注釈

矢印のサイズは [BeginArrowSize] セルで設定します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BeginArrow] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | beginarrow]  <br/> |
   
プログラムから、インデックスによって [BeginArrow] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLine** <br/> |
| セル インデックス:  <br/> |**visLineBeginArrow** <br/> |
   

