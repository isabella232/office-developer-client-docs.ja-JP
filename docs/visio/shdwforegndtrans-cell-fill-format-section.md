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
ms.openlocfilehash: 0ef3ce525edcce4ccd61f36649ead512545eef58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435041"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a>[ShdwForegndTrans] セル ([Fill Format] セクション)

図形の影に対して、塗りつぶしパターンの前景 (ストローク部分) に適用される色の透過性レベルを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|0 ～ 100  <br/> |透過性をパーセントで表します。既定値は 0% (完全に不透明) です。  <br/> |
   
## <a name="remarks"></a>注釈

値は、最も近い 0.5% 単位の値に丸められます。 値 "100%" は完全な透明を表します。 完全に透明な塗りつぶしが設定された影は、塗りつぶしがないシャドウとして図面ページに表示されますが、ページ上の他のオブジェクトとは、透明度が 0% の場合と同じように操作します。
  
この値は、[**影**] ダイアログ ボックスのスライダー コントロールを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**影**] をクリックして、[**影のオプション**] をクリックします)。この操作で設定される値は、背景と前景の両方に対する影の透過性の値を制御します。これらの値を個別に設定するには、[シェイプシート] ウィンドウでそれぞれの値を入力する必要があります。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwForegndTrans] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |[shdwforegndtrans]  <br/> |
   
プログラムから、インデックスによって [ShdwForegndTrans] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowFill** <br/> |
|セル インデックス:  <br/> |**visFillShdwForegndTrans** <br/> |
   

