---
title: '[ShdwType] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
ms.localizationpriority: medium
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: ページの既定の影の種類を指定します。
ms.openlocfilehash: 0279aaab9e608f482d0f1ecbc24e48012c087b1c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607669"
---
# <a name="shdwtype-cell-page-properties-section"></a>[ShdwType] セル ([Page Properties] セクション)

ページの既定の影の種類を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 1  <br/> | シンプル  <br/> |**visFSTSimple** <br/> |
| 2  <br/> | 斜め  <br/> |**visFSTOblique** <br/> |
|3  <br/> |Inner  <br/> |**visFSTInner** <br/> |
   
## <a name="remarks"></a>注釈

 このセルで説明するシャドウの種類は、ShapeShdwType セル (ページ上の個々の図形のシャドウ の種類) が Page Default **(visFSTPageDefault)** に設定されている場合に使用されます。 
  
シンプルな影は、ユーザー インターフェイス (UI) 内では "オフセット" と表示されます。 シンプルな影は、その図形の下の平面に影を落としているように見えます。 斜体の影は UI で "斜体" と表示され、図形が直立している平面に影を落としているように見えます。 
  
定義済みのシンプルな影と斜体の影の一覧は、[**ページ設定**] ダイアログ ボックスの [**影**] タブにある [**スタイル**] ボックスの一覧を参照してください (このダイアログ ボックスを開くには、[**デザイン**] タブで、[**ページ設定**] 矢印をクリックします)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwType] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | ShdwType  <br/> |
   
プログラムから、インデックスによって [ShapeShdwOffsetX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPage** <br/> |
| セル インデックス:  <br/> |**visPageShdwType** <br/> |
   

