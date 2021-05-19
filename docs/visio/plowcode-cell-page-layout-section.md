---
title: '[PlowCode] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251660
localization_priority: Normal
ms.assetid: e43f3d29-7def-d36e-ac64-62f0a389d415
description: 図面ページで、配置可能な図形を別の配置可能な図形の近くにドロップしたときに、これらの図形を移動して遠ざけるかどうかを指定します。
ms.openlocfilehash: 4ea85ddbaf7662305a2a82fc7f0b814019624841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420354"
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
   

