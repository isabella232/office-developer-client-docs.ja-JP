---
title: '[Spacing] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm955
localization_priority: Normal
ms.assetid: 46feb136-01ac-1303-66ab-d772c0ec41a0
description: 複数の文字間の間隔を制御します。 間隔は、1/20 ポイント単位で増減できます。
ms.openlocfilehash: 927b6203b81af453411cdd13b6f8c8342507a61b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334903"
---
# <a name="spacing-cell-character-section"></a>[Spacing] セル ([Character] セクション)

複数の文字間の間隔を制御します。 間隔は、1/20 ポイント単位で増減できます。
  
## <a name="remarks"></a>解説

このセルの値は、[**テキスト**] ダイアログ ボックスを使用して設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブで [**フォント**] 矢印をクリックします)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Spacing] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Letterspace [ *i* ] *i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Spacing] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
|行インデックス:  <br/> |**visRowCharacter** +  *i* = ** 0、1、2...  <br/> |
|セル インデックス:  <br/> |**visCharacterLetterspace** <br/> |
   

