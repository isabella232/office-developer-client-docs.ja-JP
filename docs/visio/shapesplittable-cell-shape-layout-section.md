---
title: '[ShapeSplittable] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60081
ms.localizationpriority: medium
ms.assetid: 6330304a-71f3-62b4-1b27-14495e3f12c3
description: この 1 次元図形が分割可能かどうかを示します。
ms.openlocfilehash: 31a64e466846b9d050c4993c26241933f96868d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627444"
---
# <a name="shapesplittable-cell-shape-layout-section"></a>[ShapeSplittable] セル ([Shape Layout] セクション)

この 1 次元図形が分割可能かどうかを示します。 
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | この図形は分割できません。  <br/> |**visSLOSplittableNone** <br/> |
| 1  <br/> | この図形は分割できます。  <br/> |**visSLOSplittableAllow** <br/> |
   
## <a name="remarks"></a>注釈

コネクタと他の 1 次元図形に対する既定の動作は、図面の種類によって異なります。 
  
図形の自動分割は、アプリケーション、ページ、および図形の 3 つのレベルで有効または無効にできます。既定では、アプリケーション レベルとページ レベルで分割できます。 
  
アプリケーション レベルで分割を有効または無効にするには **、[Visio** オプション] ダイアログボックスの [詳細設定] タブの [コネクタ分割を有効にする]設定を使用します ([ファイル] タブをクリックし、[オプション] をクリックし、[詳細設定] をクリック **します)。**  
  
ページでの分割を有効または無効にするには、[[PageShapeSplit]](pageshapesplit-cell-page-layout-section.md) セルを使用します。 
  
図形が 1 次元の分割可能図形を分割できるようにするには、[[ShapeSplit]](shapesplit-cell-shape-layout-section.md) セルを使用します。 
  
別の数式または **CellsU** プロパティを使用してプログラムから名前によって [ShapeSplittable] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ShapeSplittable  <br/> |
   
プログラムから、インデックスによって [ShapeSplittable] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowShapeLayout** <br/> |
| セル インデックス:  <br/> |**visSLOSplittable** <br/> |
   

