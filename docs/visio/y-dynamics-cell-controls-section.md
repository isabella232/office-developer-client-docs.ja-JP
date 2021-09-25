---
title: '[Y Dynamics] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251284
ms.localizationpriority: medium
ms.assetid: cb221974-2f1a-edb0-477b-39a3c4a64c56
description: コントロール ハンドルのアンカー ポイントの y 座標をローカル座標で表します。 アンカー ポイントは、ダイナミックス機能を使うときのラバーバンディングに使用されます。
ms.openlocfilehash: 0e60b9e2233068bc950d4649ff261dcc92e8e1a4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581743"
---
# <a name="y-dynamics-cell-controls-section"></a>[Y Dynamics] セル ([Controls] セクション)

コントロール ハンドル  *のアンカー ポイントの y*  座標をローカル座標で表します。 アンカー ポイントは、ダイナミックス機能を使うときのラバーバンディングに使用されます。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y Dynamics] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | コントロール。  *name*  .YDynwhere コントロール。  *name*  は、コントロール行の名前です。  <br/> |
   
プログラムから、インデックスによって [Y Dynamics] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionControls** <br/> |
| 行インデックス:  <br/> |**visRowControl**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visCtlYDyn** <br/> |
   

