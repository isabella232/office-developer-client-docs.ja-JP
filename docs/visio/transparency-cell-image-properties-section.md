---
title: '[Transparency] セル ([Image Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51095
localization_priority: Normal
ms.assetid: 5b265356-1602-4241-fbe1-4d5a55392a52
description: レイヤーの色の透過性レベルを指定します。
ms.openlocfilehash: 5537cbdcd49c66f3bc28a58051f6e2888a290cd3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806676"
---
# <a name="transparency-cell-image-properties-section"></a>[Transparency] セル ([Image Properties] セクション)

レイヤーの色の透過性レベルを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|0 - 100  <br/> |透過性をパーセントで表します。既定値は 0% (完全に不透明) です。  <br/> |
   
## <a name="remarks"></a>注釈

値は、最も近い 0.5% に丸められます。 100% の値は、完全に透過的です。 完全に透明な色を持つレイヤーは、レイヤーの色がないと図面ページ上で同じように表示されますとの対話ページ上の他のオブジェクトと同様に、透過性が 0% であるかのようです。 **[レイヤー プロパティ**] ダイアログ ボックスで、スライダーのつまみを使用してこの値を設定することもできます ([**ホーム**] タブの [**編集**]、[**レイヤー**] をクリックし、[**レイヤー プロパティ**] をクリック) します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、[透過性] セルへの参照を名前によって取得するには、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |Transparency  <br/> |
   
プログラムから、インデックスによって [透過性] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowImage** <br/> |
|セル インデックス:  <br/> |**visImageTransparency** <br/> |
   

