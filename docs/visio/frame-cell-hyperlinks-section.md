---
title: '[Frame] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm405
ms.localizationpriority: medium
ms.assetid: f71d8737-92ef-1124-ba4a-b7e17305bd0a
description: コンテナー アプリケーション内で、Visio アプリケーションが ActiveX の文書として開く場合、ターゲットとなるフレームの名前を表します。既定では、空の文字列です。
ms.openlocfilehash: 436a95ac60b01d951e84e6deb5d1a03887c82b47
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598592"
---
# <a name="frame-cell-hyperlinks-section"></a>[Frame] セル ([Hyperlinks] セクション)

コンテナー アプリケーション内で、Visio アプリケーションが ActiveX の文書として開く場合、ターゲットとなるフレームの名前を表します。既定では、空の文字列です。
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Frame] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ハイパーリンク  *name*  .ハイパーリンクを指定するフレーム。  *name*  は行名です  <br/> |
   
プログラムから、インデックスによって [Frame] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
| 行インデックス:  <br/> |**visRow1stHyperlink**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visHLinkFrame** <br/> |
   

