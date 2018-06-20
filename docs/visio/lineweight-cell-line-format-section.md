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
description: 図形の線の太さを指定します。線の太さを設定するには、有効な単位を使用して数値を入力します。
ms.openlocfilehash: a5207607d90ef6a79dcb3acc191521b73e2cdf54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805716"
---
# <a name="lineweight-cell-line-format-section"></a>[LineWeight] セル ([Line Format] セクション)

図形の線の太さを指定します。線の太さを設定するには、有効な単位を使用して数値を入力します。
  
## <a name="remarks"></a>注釈

LineWeight の値を [**線**] ダイアログ ボックスで設定することも ([**ホーム**] タブの [**図形**] グループで、[**行**] をクリックして、[**太さ**] をポイントおよび**他の線**] をクリック) します。
  
**Visio のオプション**] ダイアログ ボックスで指定したテキストの長さの単位を使用する測定単位を入力しない場合 (、[**ファイル**] タブをクリックし、[**オプション**] をクリック) します。 線の太さは、図面の縮尺に依存しません。 図面縮尺を変更して、線の太さは変わりません。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LineWeight] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LineWeight  <br/> |
   
プログラムから、インデックスによって [LineWeight] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLine** <br/> |
| セル インデックス:  <br/> |**visLineWeight** <br/> |
   

