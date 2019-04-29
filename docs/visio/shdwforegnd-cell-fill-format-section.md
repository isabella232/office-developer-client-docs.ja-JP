---
title: '[ShdwForegnd] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251244
localization_priority: Normal
ms.assetid: ea153390-631d-79fd-c1ba-4c281239a24e
description: 図形の影付きの塗りつぶしパターンに対して、前景 (ストローク) に使用する色を指定します。
ms.openlocfilehash: 602df83dcb88d4137b0609f9a8b1084a40148a10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422251"
---
# <a name="shdwforegnd-cell-fill-format-section"></a>[ShdwForegnd] セル ([Fill Format] セクション)

図形の影付きの塗りつぶしパターンに対して、前景 (ストローク) に使用する色を指定します。
  
## <a name="remarks"></a>注釈

色を設定するには、色のコレクションのインデックスである 0 ～ 23 の数値を入力します。
  
ユーザー設定の色を入力するには、RGB または HSL 関数を使用します。 ユーザー設定の色の値は rgb カラーで、数字ではなく rgb ( *r, g, b*) は [シェイプシート] ウィンドウに表示されます。 ユーザー設定の色を数値演算で使用する場合は、24 以上の値を指定します。 
  
図形の影付きの塗りつぶしパターンに対する前景色の透明度は、[ShdwForegndTrans] セルで設定できます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwForegnd] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [shdwforegnd]  <br/> |
   
プログラムから、インデックスによって [ShdwForegnd] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowFill** <br/> |
| セル インデックス:  <br/> |**visFillShdwForegnd** <br/> |
   

