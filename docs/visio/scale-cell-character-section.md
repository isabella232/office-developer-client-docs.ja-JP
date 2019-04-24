---
title: '[Scale] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm870
localization_priority: Normal
ms.assetid: d6fe2574-b719-f38e-b1f1-592a812f1682
description: フォントの幅を制御します。 このセルの既定値は 100% です。
ms.openlocfilehash: 60e896772ddd1d59e1a1da7f2c0e90893658c624
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341630"
---
# <a name="scale-cell-character-section"></a>[Scale] セル ([Character] セクション)

フォントの幅を制御します。 このセルの既定値は 100% です。
  
## <a name="remarks"></a>解説

フォントの幅を狭くするには、1 ～ 99% の間でパーセントを設定します。フォントの幅を広くするには、101 ～ 600% の間で設定します。
  
このセルの値は、[**テキスト**] ダイアログ ボックスを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブで [**フォント**] 矢印をクリックします)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Scale] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |文字 fontscale [ *i* ] *i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Scale] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
|行インデックス:  <br/> |**visRowCharacter** +  *i* = ** 0、1、2...  <br/> |
|セル インデックス:  <br/> |**visCharacterFontScale** <br/> |
   

