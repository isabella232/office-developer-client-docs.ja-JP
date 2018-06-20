---
title: '[FillForegndTrans] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253231
localization_priority: Normal
ms.assetid: 8b1b3904-6635-3fd1-31a9-ff32c19394af
description: 図形の塗りつぶしのパターンに対して、前景 (ストローク部分) に適用される透過性レベルを指定します。
ms.openlocfilehash: f9b09d67bc8d9ae851e86eaaa2ce1d36a92b2da2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805379"
---
# <a name="fillforegndtrans-cell-fill-format-section"></a>[FillForegndTrans] セル ([Fill Format] セクション)

図形の塗りつぶしのパターンに対して、前景 (ストローク部分) に適用される透過性レベルを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|0 - 100  <br/> |透過性をパーセントで表します。既定値は 0% (完全に不透明) です。  <br/> |
   
## <a name="remarks"></a>注釈

値は、最も近い 0.5% 単位の値に丸められます。値 100% は完全な透明を表します。塗りつぶしが完全に透明な図形は、図面ページでは塗りつぶしがない図形と同じように表示されますが、ページ上の他のオブジェクトに対しては、透過性が 0% の場合と同様な状態で相互に影響し合います。
  
スライダー コントロールを使用して、[**塗りつぶし**] ダイアログ ボックスでこの値を設定することもできます ([**ホーム**] タブの [**図形**] グループで、**塗りつぶし**を、をクリックし、[**オートフィル オプション**] をクリック) します。 この値は、前景色と背景の両方の塗りつぶしの透明度の値を制御します。 これらの値を個別に設定するのには、シェイプ シート ウィンドウで入力にする必要があります。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[FillForegndTrans] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |FillForegndTrans  <br/> |
   
プログラムから、インデックスによって [FillForegndTrans] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowFill** <br/> |
|セル インデックス:  <br/> |**visFillForegndTrans** <br/> |
   

