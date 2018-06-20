---
title: '[Frame] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm405
localization_priority: Normal
ms.assetid: f71d8737-92ef-1124-ba4a-b7e17305bd0a
description: コンテナー アプリケーション内で、Visio アプリケーションが ActiveX の文書として開く場合、ターゲットとなるフレームの名前を表します。既定では、空の文字列です。
ms.openlocfilehash: b94e5efd4a3fdf53e01f7518252852214a72c766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805453"
---
# <a name="frame-cell-hyperlinks-section"></a>[Frame] セル ([Hyperlinks] セクション)

コンテナー アプリケーション内で、Visio アプリケーションが ActiveX の文書として開く場合、ターゲットとなるフレームの名前を表します。既定では、空の文字列です。
  
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって Frame] セルへの参照を取得するには、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ハイパーリンク  *名*です。フレームの場所のハイパーリンクです。  *名前*は、行の名前  <br/> |
   
プログラムから、インデックスによって [Frame] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
| 行インデックス:  <br/> |**visRow1stHyperlink** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visHLinkFrame** <br/> |
   

