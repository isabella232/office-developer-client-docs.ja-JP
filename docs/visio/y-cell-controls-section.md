---
title: '[Y] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251282
localization_priority: Normal
ms.assetid: dd7ea5fa-1d34-44e8-5a29-69ca542aecba
description: 図形のコントロールハンドルの位置を示す y 座標を、ローカル座標で表します。
ms.openlocfilehash: 14aaa7aef7e7250baeb8ffb863244ece26a201e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360152"
---
# <a name="y-cell-controls-section"></a>[Y] セル ([Controls] セクション)

図形のコントロールハンドルの位置を示す*y*座標を、ローカル座標で表します。 
  
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | 管理.  *名前*です。ywhere コントロール  *name*は、コントロール行の名前です。  <br/> |
   
プログラムから、インデックスによって [Y] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionControls** <br/> |
| 行インデックス:  <br/> |**visRowControl** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visctly** <br/> |
   

