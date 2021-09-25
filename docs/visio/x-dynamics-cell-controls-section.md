---
title: '[X Dynamics] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1145
ms.localizationpriority: medium
ms.assetid: 9757dfb4-6d37-0517-17fe-7593ff12bbfe
description: コントロール ハンドルのアンカー ポイントの x 座標をローカル座標で表します。
ms.openlocfilehash: 9389d8e0974a5f89bfc4eee18b107dab5b0c25ca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559333"
---
# <a name="x-dynamics-cell-controls-section"></a>[X Dynamics] セル ([Controls] セクション)

コントロール ハンドルのアンカー ポイントの  *x*  座標をローカル座標で表します。 
  
## <a name="remarks"></a>注釈

アンカー ポイントは、ダイナミックス機能を使うときのラバーバンディングに使用されます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X Dynamics] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | コントロール。  *name*  .XDynwhere コントロール。  *name*  は、コントロール行の名前です。  <br/> |
   
プログラムから、インデックスによって [X Dynamics] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionControls** <br/> |
| 行インデックス:  <br/> |**visRowControl**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visCtlXDyn** <br/> |
   

