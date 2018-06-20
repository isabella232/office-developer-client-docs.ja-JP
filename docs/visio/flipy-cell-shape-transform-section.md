---
title: '[FlipY] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251198
localization_priority: Normal
ms.assetid: 062022ff-e243-2540-becd-d9b969ce83ce
description: 図形が上下反転されているかを示します。
ms.openlocfilehash: 42ee740a13c3f447f5cd4a6caa9959189320a8af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805398"
---
# <a name="flipy-cell-shape-transform-section"></a>[FlipY] セル ([Shape Transform] セクション)

図形が上下反転されているかを示します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形は上下反転されています。  <br/> |
| FALSE  <br/> | 図形は上下反転されていません。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [flipy] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [Flipy]  <br/> |
   
プログラムから、インデックスによって [flipy] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowXFormOut** <br/> |
| セル インデックス:  <br/> |**visXFormFlipY** <br/> |
   

