---
title: '[ShapeShdwType] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033173
ms.localizationpriority: medium
ms.assetid: 1461148d-90a9-6f7c-1b28-9310ffaf0e3b
description: 図形の影の種類を指定します。
ms.openlocfilehash: a2c82e41d00151202ee47c2863364e59a3688a66
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598130"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a>[ShapeShdwType] セル ([Fill Format] セクション)

図形の影の種類を指定します。 
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |ページの既定値を使用します (既定値)。  <br/> |**visFSTPageDefault** <br/> |
|1  <br/> |シンプル  <br/> |**visFSTSimple** <br/> |
|2  <br/> |斜め  <br/> |**visFSTOblique** <br/> |
   
## <a name="remarks"></a>注釈

このセルを使用して、ページの既定とは異なる図形の影を適用します (ページの既定のシャドウの種類は、[ページのプロパティ] セクションの [ShdwType] セルで定義されます)。
  
シンプルな影は、ユーザー インターフェイス (UI) では "オフセット" と表示されます。 シンプルな影は、その図形の下の平面に影を落としているように見えます。 斜体の影は UI では "斜体" と表示され、その図形が直立している平面に影を落としているように見えます。 
  
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
   

