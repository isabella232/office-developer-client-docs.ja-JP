---
title: '[TxtLocPinX] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
localization_priority: Normal
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: テキスト ブロックの回転中心の x 座標を、テキスト ブロックの原点に関連付けます。 既定の数式は次のとおりです。
ms.openlocfilehash: 390f8129e8000a043969eda0ab1c8e4ef62515ef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425856"
---
# <a name="txtlocpinx-cell-text-transform-section"></a>[TxtLocPinX] セル ([Text Transform] セクション)

テキスト ブロック  *の回転*  中心の x 座標を、テキスト ブロックの原点に関連付けます。 既定の数式は次のとおりです。 
  
= TxtWidth \* 0.5
  
この数式では、テキスト ブロックの水平方向の中心が回転の中心になります。
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtLocPinX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | TxtLocPinX  <br/> |
   
プログラムから、インデックスによって [TxtLocPinX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス :  <br/> |**visRowTextXForm** <br/> |
| セル インデックス:  <br/> |**visXFormLocPinX** <br/> |
   

