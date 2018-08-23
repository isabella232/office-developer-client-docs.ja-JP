---
title: '[ResizeMode] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251203
localization_priority: Normal
ms.assetid: 49816e46-fa83-3ee4-1451-9c85fbd0f519
description: 図形に対して現在設定されているサイズ変更の動作の方法を示します。
ms.openlocfilehash: a32f5dbc935e85a49ab585073ca6a31215fd102a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806261"
---
# <a name="resizemode-cell-shape-transform-section"></a>[ResizeMode] セル ([図形変換] セクション)

図形に対して現在設定されているサイズ変更の動作の方法を示します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |グループの設定を使用します。  <br/> |**visXFormResizeDontCare** <br/> |
|1  <br/> |位置のみを変更します。  <br/> |**visXFormResizeSpread** <br/> |
|2  <br/> |グループに合わせてサイズを変更します。  <br/> |**visXFormResizeScale** <br/> |
   
## <a name="remarks"></a>注釈

[**動作**] タブ、[**動作**] ダイアログ ボックスでこの値を設定することもできます ([[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] で、[**動作**] をクリック) します。 別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ResizeMode] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |ResizeMode  <br/> |
   
プログラムから、インデックスによって [ResizeMode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowXFormOut** <br/> |
|セル インデックス:  <br/> |**visXFormResizeMode** <br/> |
   

