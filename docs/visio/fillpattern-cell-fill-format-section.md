---
title: '[FillPattern] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm375
localization_priority: Normal
ms.assetid: dac82a4f-4508-541a-e118-7d79df987232
description: 図形の塗りつぶしのパターンを指定します。 ユーザー設定の塗りつぶしのパターンを指定するには、このセルで USE 関数を使用します。
ms.openlocfilehash: 340ccdc9f3819fb29e210832107e270bd302433c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322436"
---
# <a name="fillpattern-cell-fill-format-section"></a>[FillPattern] セル ([Fill Format] セクション)

図形の塗りつぶしのパターンを指定します。 ユーザー設定の塗りつぶしのパターンを指定するには、このセルで USE 関数を使用します。
  
|**値**|**説明**|
|:-----|:-----|
|.0  <br/> |なし (透明な塗りつぶし)。  <br/> |
|1-d  <br/> |前景の色。  <br/> |
|2 ～ 40  <br/> |さまざまな塗りつぶしのパターン。入力した値は [**塗りつぶし**] ダイアログ ボックスに表示されるインデックス付きエントリに対応します。  <br/> |
   
## <a name="remarks"></a>解説

この値は、[**塗りつぶし**] ダイアログ ボックスを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**塗りつぶし**] クリックして、[**塗りつぶしのオプション**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [FillPattern] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |fillpattern]  <br/> |
   
プログラムから、インデックスによって [FillPattern] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowFill** <br/> |
|セル インデックス:  <br/> |**visFillPattern** <br/> |
   

