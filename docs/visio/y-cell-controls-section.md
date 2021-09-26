---
title: '[Y] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251282
ms.localizationpriority: medium
ms.assetid: dd7ea5fa-1d34-44e8-5a29-69ca542aecba
description: 図形のコントロール ハンドルの位置をローカル座標で示す y 座標を表します。
ms.openlocfilehash: 5fc0fa7d0219993d4790eece205010cce33fca82
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597710"
---
# <a name="y-cell-controls-section"></a>[Y] セル ([Controls] セクション)

図形のコントロール ハンドルの位置をローカル座標で示す  *y*  座標を表します。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | コントロール。  *name*  .Ywhere コントロール。  *name*  は、コントロール行の名前です。  <br/> |
   
プログラムから、インデックスによって [Y] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionControls** <br/> |
| 行インデックス:  <br/> |**visRowControl**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visCtlY** <br/> |
   

