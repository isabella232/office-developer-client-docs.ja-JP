---
title: '[X Dynamics] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1145
localization_priority: Normal
ms.assetid: 9757dfb4-6d37-0517-17fe-7593ff12bbfe
description: コントロールハンドルのアンカーポイントの x 座標を、ローカル座標で表します。
ms.openlocfilehash: 7aef1fe779ae9b862e88eccf0112eb8696377858
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432129"
---
# <a name="x-dynamics-cell-controls-section"></a>[X Dynamics] セル ([Controls] セクション)

コントロールハンドルのアンカーポイントの*x*座標を、ローカル座標で表します。 
  
## <a name="remarks"></a>注釈

アンカー ポイントは、ダイナミックス機能を使うときのラバーバンディングに使用されます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X Dynamics] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | 管理.  *名前*です。XDynwhere コントロール  *name*は、コントロール行の名前です。  <br/> |
   
プログラムから、インデックスによって [X Dynamics] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionControls** <br/> |
| 行インデックス:  <br/> |**visRowControl** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visCtlXDyn** <br/> |
   

