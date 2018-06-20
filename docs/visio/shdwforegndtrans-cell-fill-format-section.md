---
title: '[ShdwForegndTrans] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253253
localization_priority: Normal
ms.assetid: c42d4d2e-f8f0-bc5b-6018-4bb4ffa81b64
description: 図形の影に対して、塗りつぶしパターンの前景 (ストローク部分) に適用される色の透過性レベルを指定します。
ms.openlocfilehash: 5fd385fc2f46f1ff8eedc961833813ec16ba7b73
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806448"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a>[ShdwForegndTrans] セル ([Fill Format] セクション)

図形の影に対して、塗りつぶしパターンの前景 (ストローク部分) に適用される色の透過性レベルを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|0 - 100  <br/> |透過性をパーセントで表します。既定値は 0% (完全に不透明) です。  <br/> |
   
## <a name="remarks"></a>注釈

値は、最も近い 0.5% に丸められます。 100% の値は、完全に透過的です。 完全に透明な塗りつぶしが設定されている影は、塗りつぶしがない影と図面ページ上で同じように表示されますとの対話のページで他のオブジェクトと同じ方法で、透過性が 0% であるかのようです。
  
[**影**] ダイアログ ボックスで、スライダーのつまみを使用してこの値を設定することもできます ([**ホーム**] タブの [**図形**] グループで、**シャドウ**] をクリックし、[**影のオプション**] をクリック) します。 この値は、前景色と背景の両方の影の透明度の値を制御します。 これらの値を個別に設定するのには、シェイプ シート ウィンドウで入力にする必要があります。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShdwForegndTrans] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |ShdwForegndTrans  <br/> |
   
プログラムから、インデックスによって [ShdwForegndTrans] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowFill** <br/> |
|セル インデックス:  <br/> |**visFillShdwForegndTrans** <br/> |
   

