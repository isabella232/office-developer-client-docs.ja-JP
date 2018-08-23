---
title: '[ShapeShdwType] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033173
localization_priority: Normal
ms.assetid: 1461148d-90a9-6f7c-1b28-9310ffaf0e3b
description: 図形の影の種類を指定します。
ms.openlocfilehash: b96ad4a877d72bf4457ec3cf038a29a2b414e0f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806418"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a>[ShapeShdwType] セル ([塗りつぶしの書式設定] セクション)

図形の影の種類を指定します。 
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |ページの既定値を使用します (既定値)。  <br/> |**visFSTPageDefault** <br/> |
|1  <br/> |シンプルな影です。  <br/> |**visFSTSimple** <br/> |
|2  <br/> |斜体の影です。  <br/> |**visFSTOblique** <br/> |
   
## <a name="remarks"></a>注釈

(デフォルト ページの影の種類は [ページ プロパティ] セクションの [shdwtype] セルで定義されている) ページの既定値とは異なる図形の影を適用するのにには、このセルを使用します。
  
シンプルな影は、ユーザー インターフェイス (UI) 内のオフセットの影として説明します。 シンプルな影は図形の背後にある平行な平面上にシャドウされている図形の効果を示します。 斜体の影は、UI 内の斜体の影として説明され、図形に垂直な平面に影の効果を与えます。 
  
事前定義されたシンプルな影と斜体の影の種類のリストは、[**影**] ダイアログ ボックスの [**スタイル**] ボックスを参照してください (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**影**] をクリックして、[**影のオプション**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapeShdwType] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |ShapeShdwType  <br/> |
   
プログラムから、インデックスによって [ShapeShdwType] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowFill** <br/> |
|セル インデックス:  <br/> |**visFillShdwType** <br/> |
   

