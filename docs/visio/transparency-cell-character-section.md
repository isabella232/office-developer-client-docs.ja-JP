---
title: '[Transparency] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50135
localization_priority: Normal
ms.assetid: ab835a1a-9e90-126e-279f-463882c48e93
description: 図形のテキストの色に適用される透過性レベルを指定します。
ms.openlocfilehash: 8619ec25372ae163fff1759aca36ff6693820e39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280984"
---
# <a name="transparency-cell-character-section"></a>[Transparency] セル ([Character] セクション)

図形のテキストの色に適用される透過性レベルを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|0 ～ 100  <br/> |透過性をパーセントで表します。既定値は 0% (完全に不透明) です。  <br/> |
   
## <a name="remarks"></a>解説

値は、最も近い 0.5% 単位の値に丸められます。値 "100%" は完全な透明を表します。テキストが完全に透明な図形は、図面ページではテキストがない図形と同じように表示されますが、ページ上の他のオブジェクトに対しては、透過性が 0% の場合と同様な状態で相互に影響し合います。
  
この値は、[**テキスト**] ダイアログボックスの [**フォント**] タブのスライダーコントロールを使用して設定することもできます ([**ホーム**] タブの [**フォント**] 矢印をクリックします)。 
  
[Character] セクションに複数の行が含まれる場合は、[Transparency] セルには、図形のテキストのサブ範囲に適用される書式設定情報が表示されます。複数の行が含まれない場合は、このセルには、すべての図形のテキストに対する書式設定情報が表示されます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Transparency] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |<1>、2、3 ** ... ** を指定します。  <br/> |
   
プログラムから、インデックスによって [Transparency] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
|行インデックス:  <br/> |**visRowCharacter** +  *i* = ** 0、1、2...  <br/> |
|セル インデックス:  <br/> |**visCharacterColorTrans** <br/> |
   

