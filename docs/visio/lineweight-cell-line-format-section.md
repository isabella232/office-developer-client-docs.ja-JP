---
title: '[LineWeight] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm585
ms.localizationpriority: medium
ms.assetid: 16b0e293-eeef-34b4-aeb0-4472815dd543
description: 図形の線の太さを指定します。線の太さを設定するには、有効な単位を使用して数値を入力します。
ms.openlocfilehash: c38e1b2736c409e3362586bc651a4815394511ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618638"
---
# <a name="lineweight-cell-line-format-section"></a>[LineWeight] セル ([Line Format] セクション)

図形の線の太さを指定します。線の太さを設定するには、有効な単位を使用して数値を入力します。
  
## <a name="remarks"></a>注釈

LineWeight の値は、[**線**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを表示するには、[**ホーム**] タブの [**図形**] で、[**線**] をクリックし、[**太さ**] をポイントして、[**その他の線**] をクリックします)。
  
単位を入力しない場合は **、[Visio オプション**] ダイアログ ボックスで指定したテキストの測定単位が使用されます ([ファイル]タブをクリックし、[オプション] をクリック **します**)。 線の太さは、図面の縮尺による影響を受けません。 図面の縮尺を変更しても、線の太さは変わりません。 
  
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
   

