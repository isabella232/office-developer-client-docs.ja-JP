---
title: '[ShdwType] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
localization_priority: Normal
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: ページの既定の影の種類を指定します。
ms.openlocfilehash: f1fc72484d94788ca2798760ca935c89c3e841ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424099"
---
# <a name="shdwtype-cell-page-properties-section"></a>[ShdwType] セル ([Page Properties] セクション)

ページの既定の影の種類を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 1   <br/> | 単純  <br/> |**visFSTSimple** <br/> |
| 2   <br/> | 斜体  <br/> |**visFSTOblique** <br/> |
|3   <br/> |内側  <br/> |**visFSTInner** <br/> |
   
## <a name="remarks"></a>注釈

 このセルに記述されている影の種類は、[shapeshdwtype] セル (ページ上の個々の図形の影の種類) が [ページの既定値 (**visFSTPageDefault** )] に設定されている場合に使用します。 
  
シンプルな影は、ユーザー インターフェイス (UI) 内では "オフセット" と表示されます。 シンプルな影は、その図形の下の平面に影を落としているように見えます。 斜体の影は UI で "斜体" と表示され、図形が直立している平面に影を落としているように見えます。 
  
定義済みのシンプルな影と斜体の影の一覧は、[**ページ設定**] ダイアログ ボックスの [**影**] タブにある [**スタイル**] ボックスの一覧を参照してください (このダイアログ ボックスを開くには、[**デザイン**] タブで、[**ページ設定**] 矢印をクリックします)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwType] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [shdwtype]  <br/> |
   
プログラムから、インデックスによって [ShapeShdwOffsetX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPage** <br/> |
| セル インデックス:  <br/> |**visPageShdwType** <br/> |
   

