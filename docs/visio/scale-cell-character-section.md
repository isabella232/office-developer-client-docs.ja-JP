---
title: '[Scale] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm870
ms.localizationpriority: medium
ms.assetid: d6fe2574-b719-f38e-b1f1-592a812f1682
description: フォントの幅を制御します。このセルの既定値は 100% です。
ms.openlocfilehash: 50708cd670f7d048e2c0321e5752d1826cbf8091
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607753"
---
# <a name="scale-cell-character-section"></a>[Scale] セル ([Character] セクション)

フォントの幅を制御します。このセルの既定値は 100% です。
  
## <a name="remarks"></a>注釈

フォントの幅を狭くするには、1 ～ 99% の間でパーセントを設定します。フォントの幅を広くするには、101 ～ 600% の間で設定します。
  
このセルの値は、[**テキスト**] ダイアログ ボックスを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブで [**フォント**] 矢印をクリックします)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Scale] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Char.FontScale[ *i*  ]  *ここで、i*  = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Scale] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
|行インデックス:  <br/> |**visRowCharacter**  +  *i* *=* 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visCharacterFontScale** <br/> |
   

