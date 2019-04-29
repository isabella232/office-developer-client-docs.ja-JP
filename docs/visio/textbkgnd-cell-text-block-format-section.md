---
title: '[TextBkgnd] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251267
localization_priority: Normal
ms.assetid: a238bf1c-1acd-eacd-22f3-a48acaaa4549
description: 図形のテキストの背景色を指定します。
ms.openlocfilehash: 2450bf0cb0e013c0f9310eacfca0f5a20e7e6063
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406543"
---
# <a name="textbkgnd-cell-text-block-format-section"></a>[TextBkgnd] セル ([Text Block Format] セクション)

図形のテキストの背景色を指定します。
  
## <a name="remarks"></a>注釈

[TextBkgnd] セルには、0 ～ 24、または 255 のいずれかの値を指定できます。 値0と 255 ( *visTxtBlklOpaque*) は、両方とも透明なテキストの背景を示します。 
  
ユーザー設定の色を入力するには、RGB または HSL 関数に 1 を加算したもの、たとえば RGB(255,127,255)+1 を使用します。 ユーザー設定の色の値は rgb カラーで、数字ではなく rgb ( *r, g, b*) + 1 が [シェイプシート] ウィンドウに表示されます。 ユーザー設定の色を数値演算で使用する場合は、25 以上の値を指定します。 
  
テキストの背景色の透過性は [TextBkgndTrans] セルで設定できます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TextBkgnd] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[textbkgnd]  <br/> |
   
プログラムから、インデックスによって [TextBkgnd] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowText** <br/> |
|セル インデックス:  <br/> |**visTxtBlkBkgnd** <br/> |
   

