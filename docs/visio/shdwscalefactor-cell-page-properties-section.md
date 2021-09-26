---
title: '[ShdwScaleFactor] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60083
ms.localizationpriority: medium
ms.assetid: 10979706-6dfe-5241-e862-3f94716d14fa
description: 図形の影を拡大または縮小する割合を、パーセントで指定します。
ms.openlocfilehash: bc5f5fb3fa4fc3d922c0ac8e629f784212a5e3c5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603523"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a>[ShdwScaleFactor] セル ([Page Properties] セクション)

図形の影を拡大または縮小する割合を、パーセントで指定します。 
  
## <a name="remarks"></a>注釈

各シャドウには影付きピンの位置があります。これは、図形のピンに対応するシャドウ上のポイントです。 たとえば、図形のピンが図形の中央にある場合、影付きピンの位置は影の中心のポイントになります。 単純な影にスケールを適用する場合、倍率は影付きピンの位置の中央に配置されます。斜めの影にスケールを適用すると、斜め方向に倍率が適用されます。 
  
 この割合は、図形のシャドウの種類が Page Default (ShapeShdwType セルが ** visFSTPageDefault ** ) に設定されている場合に使用されます。 
  
個々の図形に対してこの動作を設定するには、[Fill Format] セクションで [ShapeShdwScaleFactor] セルを使用します。
  
この値は、[**ページ設定**] ダイアログ ボックスの [**影**] タブにある [**倍率**] ボックスの値に対応しています (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックします)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShdwScaleFactor] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | ShdwScaleFactor  <br/> |
   
プログラムから、インデックスによって [ShdwScaleFactor] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPage** <br/> |
| セル インデックス:  <br/> |**visPageShdwScaleFactor** <br/> |
   

