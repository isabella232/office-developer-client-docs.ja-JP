---
title: '[Color] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm160
localization_priority: Normal
ms.assetid: 1c9aab2e-6c2f-0684-4e66-c35ac71883d6
description: 図形のテキストに使用する色を指定します。
ms.openlocfilehash: a27d957781ca9a784e7ab9d5c1ce4f533b9a55ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341840"
---
# <a name="color-cell-character-section"></a>[Color] セル ([Character] セクション)

図形のテキストに使用する色を指定します。
  
## <a name="remarks"></a>解説

色を設定するには、0 ～ 23 の数値を入力します。
  
ユーザー設定の色を入力するには、RGB または HSL 関数を使用します。 ユーザー設定の色の値は rgb カラーで、数字ではなく rgb ( *r, g, b*) は [シェイプシート] ウィンドウに表示されます。 ユーザー設定の色を数値演算で使用する場合は、24 以上の値を指定します。 
  
テキストの色の透過性を設定するには、[Transparency] セルを使用します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Color] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |文字の色 [ *i* ] = ** <1>、2、3、...  <br/> |
   
プログラムから、インデックスによって [Color] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
|行インデックス:  <br/> |**visRowCharacter** +  *i* = ** 0、1、2、...  <br/> |
|セル インデックス:  <br/> |**visCharacterColor** <br/> |
   

