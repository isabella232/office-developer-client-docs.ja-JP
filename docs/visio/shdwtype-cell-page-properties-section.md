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
ms.openlocfilehash: 1fc5c31a723d5d409110d94ff543a45dadabf264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806467"
---
# <a name="shdwtype-cell-page-properties-section"></a>[ShdwType ] セル ([ページのプロパティ] セクション)

ページの既定の影の種類を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 1  <br/> | シンプルな影です。  <br/> |**visFSTSimple** <br/> |
| 2  <br/> | 斜体の影です。  <br/> |**visFSTOblique** <br/> |
|3  <br/> |内部  <br/> |**visFSTInner** <br/> |
   
## <a name="remarks"></a>注釈

 ShapeShdwType セル (ページ上の個々 の図形の影の種類) がページの既定値 (**visFSTPageDefault** ) に設定するたびに、このセルに記載されている影の種類が使用されます。 
  
シンプルな影は、ユーザー インターフェイス (UI) 内のオフセットの影として説明します。 シンプルな影は、その背後にある程度の距離の平面上にシャドウされている図形の効果を示します。 斜体の影は、UI 内の斜体の影として説明され、図形に垂直な平面に影の効果を与えます。 
  
定義済みのシンプルな影と斜体の影の一覧は、[**ページ設定**] ダイアログ ボックスの [**影**] タブにある [**スタイル**] ボックスの一覧を参照してください (このダイアログ ボックスを開くには、[**デザイン**] タブで、[**ページ設定**] 矢印をクリックします)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwType] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [Shdwtype]  <br/> |
   
プログラムから、インデックスによって [ShapeShdwOffsetX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPage** <br/> |
| セル インデックス:  <br/> |**visPageShdwType** <br/> |
   

