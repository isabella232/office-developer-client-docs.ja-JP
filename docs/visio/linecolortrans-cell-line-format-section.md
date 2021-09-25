---
title: '[LineColorTrans] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50120
ms.localizationpriority: medium
ms.assetid: b68054b5-7efd-1156-9dc1-5ec94e18d227
description: 図形の線の色の透過性レベルを指定します。
ms.openlocfilehash: fe36c5f372015ca70b2e40f71fa0b7cf39027a04
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582590"
---
# <a name="linecolortrans-cell-line-format-section"></a>[LineColorTrans] セル ([Line Format] セクション)

図形の線の色の透過性レベルを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|0 ～ 100  <br/> |透過性をパーセントで表します。既定値は 0% (完全に不透明) です。  <br/> |
   
## <a name="remarks"></a>注釈

値は、最も近い 0.5% 単位の値に丸められます。値 "100%" は完全な透明を表します。完全に透明な色の線をもつ図形は、図面ページでは線がない図形と同じように表示されますが、ページ上の他のオブジェクトに対しては、透過性が 0% の場合と同様な状態で相互に影響し合います。 
  
この値は、[**線**] ダイアログ ボックスのスライダー コントロールを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**線**] をクリックし、[**太さ**] をポイントして、[**その他の線**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineColorTrans] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |LineColorTrans  <br/> |
   
プログラムから、インデックスによって [LineColorTrans] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLine** <br/> |
|セル インデックス:  <br/> |**visLineColorTrans** <br/> |
   

