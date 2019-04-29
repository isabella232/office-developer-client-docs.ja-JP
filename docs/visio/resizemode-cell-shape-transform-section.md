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
ms.openlocfilehash: 7e9080fcd4604e2dbdc1dae31992f05e5b512213
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421964"
---
# <a name="resizemode-cell-shape-transform-section"></a>[ResizeMode] セル ([Shape Transform] セクション)

図形に対して現在設定されているサイズ変更の動作の方法を示します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|.0  <br/> |グループの設定を使用します。  <br/> |**visXFormResizeDontCare** <br/> |
|1   <br/> |位置のみを変更します。  <br/> |**visXFormResizeSpread** <br/> |
|2   <br/> |グループに合わせてサイズを変更します。  <br/> |**visXFormResizeScale** <br/> |
   
## <a name="remarks"></a>注釈

この値は、[**基本動作**] ダイアログボックス ([[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] グループで、[**基本動作**] をクリック) の [**動作**] タブで設定することもできます。 別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ResizeMode] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[resizemode]  <br/> |
   
プログラムから、インデックスによって [ResizeMode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowXFormOut** <br/> |
|セル インデックス:  <br/> |**visXFormResizeMode** <br/> |
   

