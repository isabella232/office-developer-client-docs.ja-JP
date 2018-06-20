---
title: '[ShdwPattern] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm935
localization_priority: Normal
ms.assetid: eca73b80-9835-9011-1dce-187ccee92e76
description: 図形の影の塗りつぶしパターンを指定します。
ms.openlocfilehash: fd24a8d23d62436a6d81cf6b8049dcabe47db677
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806455"
---
# <a name="shdwpattern-cell-fill-format-section"></a>[ShdwPattern] セル ([Fill Format] セクション)

図形の影の塗りつぶしパターンを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |なし (透明な塗りつぶし)  <br/> |
|1  <br/> |無地の前景色  <br/> |
|2-40  <br/> |さまざまなパターン  <br/> |
   
## <a name="remarks"></a>注釈

塗りつぶしのパターンを設定するには、番号を入力、0 から 40、パターンのコレクションのインデックスとなっています。 塗りつぶしパターンのコレクションを表示するには、[**塗りつぶし**] ダイアログ ボックスで ([**ホーム**] タブの [**図形**] グループで、**塗りつぶし**] をクリックし、[**オートフィル オプション**] をクリック) します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShdwPattern] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |ShdwPattern  <br/> |
   
プログラムから、インデックスによって [ShdwPattern] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowFill** <br/> |
|セル インデックス:  <br/> |**visFillShdwPattern** <br/> |
   

