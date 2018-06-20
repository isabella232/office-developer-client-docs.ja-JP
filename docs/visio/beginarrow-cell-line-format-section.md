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
description: 最初の頂点には、矢印やその他の書式の端点に 1 行かどうかを示します。 0 から 45 に番号を入力、または使用して機能のユーザー設定の線の端点では、名前の線] ダイアログ ボックスを使用します。
ms.openlocfilehash: c6d5a66d76cfea61b1c9923c5b904dadec5495f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804795"
---
# <a name="beginarrow-cell-line-format-section"></a>[BeginArrow] セル ([Line Format] セクション)

最初の頂点には、矢印やその他の書式の端点に 1 行かどうかを示します。 0 から 45 に番号を入力、または使用して機能のユーザー設定の線の端点では、名前の**線**] ダイアログ ボックスを使用します。 
  
|**値**|**説明**|
|:-----|:-----|
| 0  <br/> | 矢印を付けません。  <br/> |
| 1-45  <br/> | さまざまな矢印のスタイル、[**線**] ダイアログ ボックス内のエントリのインデックスを作成します。  <br/> |
   
## <a name="remarks"></a>備考

矢印のサイズは [BeginArrowSize] セルで設定します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[BeginArrow] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | BeginArrow  <br/> |
   
プログラムから、インデックスによって [BeginArrow] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLine** <br/> |
| セル インデックス:  <br/> |**visLineBeginArrow** <br/> |
   

