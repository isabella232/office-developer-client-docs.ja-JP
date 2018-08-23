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
ms.openlocfilehash: f39109a296949d23142017661bb55f0708402d8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806462"
---
# <a name="shdwforegnd-cell-fill-format-section"></a>[ShdwForegnd] セル ([塗りつぶしの書式設定] セクション)

図形の影付きの塗りつぶしパターンに対して、前景 (ストローク) に使用する色を指定します。
  
## <a name="remarks"></a>注釈

色を設定するには、色のコレクションのインデックスである 0 ～ 23 の数値を入力します。
  
独自の色を入力するには、RGB または HSL 関数を使用します。 その RGB カラーでは、ユーザー設定の色の値と、数値ではなく RGB ( *r, g, b*)、[シェイプ シート] ウィンドウが表示されます。 数値演算で使用する場合は、24 以上の値があるユーザー設定の色です。 
  
図形の影付きの塗りつぶしパターンに対する前景色の透明度は、[ShdwForegndTrans] セルで設定できます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwForegnd] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | ShdwForegnd  <br/> |
   
プログラムから、インデックスによって [ShdwForegnd] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowFill** <br/> |
| セル インデックス:  <br/> |**visFillShdwForegnd** <br/> |
   

