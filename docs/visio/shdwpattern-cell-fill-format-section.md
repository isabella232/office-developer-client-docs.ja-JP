---
title: '[ShdwPattern] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm935
ms.localizationpriority: medium
ms.assetid: eca73b80-9835-9011-1dce-187ccee92e76
description: 図形の影の塗りつぶしパターンを指定します。
ms.openlocfilehash: 2216cc18149cf36be52b3c034d8c0634fa40e9b8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559547"
---
# <a name="shdwpattern-cell-fill-format-section"></a>[ShdwPattern] セル ([Fill Format] セクション)

図形の影の塗りつぶしパターンを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |なし (透明な塗りつぶし)  <br/> |
|1  <br/> |無地の前景色  <br/> |
|2 - 40  <br/> |さまざまなパターン  <br/> |
   
## <a name="remarks"></a>注釈

塗りつぶしパターンを設定するには、パターンのコレクションのインデックスである 0 ～ 40 の数値を入力します。塗りつぶしパターンのコレクションは、[**塗りつぶし**] ダイアログ ボックスで参照できます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**塗りつぶし**] をクリックして、[**塗りつぶしのオプション**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwPattern] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |ShdwPattern  <br/> |
   
プログラムから、インデックスによって [ShdwPattern] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowFill** <br/> |
|セル インデックス:  <br/> |**visFillShdwPattern** <br/> |
   

