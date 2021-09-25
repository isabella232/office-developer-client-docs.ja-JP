---
title: '[TextBkgnd] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251267
ms.localizationpriority: medium
ms.assetid: a238bf1c-1acd-eacd-22f3-a48acaaa4549
description: 図形のテキストの背景色を指定します。
ms.openlocfilehash: f8c564a3caf6685ffe0cb0babd3c06cb9a89b11e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559410"
---
# <a name="textbkgnd-cell-text-block-format-section"></a>[TextBkgnd] セル ([Text Block Format] セクション)

図形のテキストの背景色を指定します。
  
## <a name="remarks"></a>注釈

[TextBkgnd] セルには、0 ～ 24、または 255 のいずれかの値を指定できます。 値 0 と 255 *(visTxtBlklOpaque) は*、両方とも透明なテキストの背景を示します。 
  
ユーザー設定の色を入力するには、RGB または HSL 関数に 1 を加算したもの、たとえば RGB(255,127,255)+1 を使用します。 カスタム色の値は RGB 色で、RGB( *r, g, b*)+1 は数値ではなく、シェイプシート ウィンドウに表示されます。 ユーザー設定の色を数値演算で使用する場合は、25 以上の値を指定します。 
  
テキストの背景色の透過性は [TextBkgndTrans] セルで設定できます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TextBkgnd] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |TextBkgnd  <br/> |
   
プログラムから、インデックスによって [TextBkgnd] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowText** <br/> |
|セル インデックス:  <br/> |**visTxtBlkBkgnd** <br/> |
   

