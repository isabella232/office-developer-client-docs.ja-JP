---
title: '[TextBkgndTrans] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253240
localization_priority: Normal
ms.assetid: b2f9d317-cc42-bec5-66f9-f988bcbdcc24
description: 図形のテキスト ブロックの背景色に適用される透過性レベルを指定します。
ms.openlocfilehash: d9fee430cb2ccd19e8d6069e7561a8fef409a62e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806628"
---
# <a name="textbkgndtrans-cell-text-block-format-section"></a>[TextBkgndTrans] セル ([テキスト ブロックの書式設定] セクション)

図形のテキスト ブロックの背景色に適用される透過性レベルを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|
          0 ～ 100
  <br/> |透過性をパーセントで表します。既定値は 0% (完全に不透明) です。  <br/> |
   
## <a name="remarks"></a>注釈

値は、最も近い 0.5% 単位の値に丸められます。値 "100%" は完全な透明を表します。テキストの背景が完全に透明な図形は、図面ページでは背景がない図形と同じように表示されますが、ページ上の他のオブジェクトに対しては、透過性が 0% の場合と同様な状態で相互に影響し合います。
  
この値は、[**テキスト**] ダイアログ ボックスの [**フォント**] タブのスライダー コントロールを使用して設定することもできます (このタブを開くには、[**ホーム**] タブの [**フォント**] 矢印をクリックします)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TextBkgndTrans] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |TextBkgndTrans  <br/> |
   
プログラムから、インデックスによって [TextBkgndTrans] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowText** <br/> |
|セル インデックス:  <br/> |**visTxtBlkBkgndTrans** <br/> |
   

