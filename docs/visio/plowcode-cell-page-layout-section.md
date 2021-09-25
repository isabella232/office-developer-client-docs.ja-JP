---
title: '[PlowCode] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251660
ms.localizationpriority: medium
ms.assetid: e43f3d29-7def-d36e-ac64-62f0a389d415
description: 図面ページで、配置可能な図形を別の配置可能な図形の近くにドロップしたときに、これらの図形を移動して遠ざけるかどうかを指定します。
ms.openlocfilehash: de96a824176c4407527ef96b18a0f1695305070c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608082"
---
# <a name="plowcode-cell-page-layout-section"></a>[PlowCode] セル ([Page Layout] セクション)

図面ページで、配置可能な図形を別の配置可能な図形の近くにドロップしたときに、これらの図形を移動して遠ざけるかどうかを指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |図形を移動しません。  <br/> |**visPLOPlowNone** <br/> |
|1  <br/> |図形を移動します。  <br/> |**visPLOPlowAll** <br/> |
   
## <a name="remarks"></a>注釈

[ページ設定] ダイアログ ボックスの [レイアウトとルーティング] タブ([デザイン] タブの [ページ設定] 矢印をクリック)で、[他の図形をドロップ時に移動] チェック ボックスを使用して、このセルの値を設定することもできます。   
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PlowCode] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |PlowCode  <br/> |
   
プログラムから、インデックスによって [PlowCode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOPlowCode** <br/> |
   

