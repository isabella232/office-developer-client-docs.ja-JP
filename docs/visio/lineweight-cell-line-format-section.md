---
title: '[LineWeight] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm585
localization_priority: Normal
ms.assetid: 16b0e293-eeef-34b4-aeb0-4472815dd543
description: 図形の線の太さを指定します。 線の太さを設定するには、有効な単位を使用して数値を入力します。
ms.openlocfilehash: 654a93f939226bedab2e40ab591dad0e3f872267
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412248"
---
# <a name="lineweight-cell-line-format-section"></a>[LineWeight] セル ([Line Format] セクション)

図形の線の太さを指定します。 線の太さを設定するには、有効な単位を使用して数値を入力します。
  
## <a name="remarks"></a>注釈

LineWeight の値は、[**線**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを表示するには、[**ホーム**] タブの [**図形**] で、[**線**] をクリックし、[**太さ**] をポイントして、[**その他の線**] をクリックします)。
  
単位が入力されていない場合は、[ **Visio のオプション**] ダイアログボックスで指定されたテキストの測定単位を使用します ([**ファイル**] タブをクリックし、[**オプション**] をクリックします)。 線の太さは、図面の縮尺による影響を受けません。 図面の縮尺を変更しても、線の太さは変わりません。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineWeight] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LineWeight  <br/> |
   
プログラムから、インデックスによって [LineWeight] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLine** <br/> |
| セル インデックス:  <br/> |**visLineWeight** <br/> |
   

