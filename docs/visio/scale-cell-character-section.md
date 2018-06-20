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
description: フォントの幅を制御します。このセルの既定値は 100% です。
ms.openlocfilehash: fedbc0aec23320d03ca358f34babda56eaab31e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806348"
---
# <a name="scale-cell-character-section"></a>[Scale] セル ([Character] セクション)

フォントの幅を制御します。このセルの既定値は 100% です。
  
## <a name="remarks"></a>注釈

フォントの幅を狭くするには、1 ～ 99% の間でパーセントを設定します。フォントの幅を広くするには、101 ～ 600% の間で設定します。
  
**テキスト**] ダイアログ ボックスを使用してこのセルの値を設定することもできます ([**ホーム**] タブで、[**フォント**の矢印] をクリック) します。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって Scale] セルへの参照を取得するには、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Char.FontScale [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [Scale] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
|行インデックス:  <br/> |**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visCharacterFontScale** <br/> |
   

