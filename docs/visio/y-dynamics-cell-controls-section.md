---
title: '[Y Dynamics] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251284
localization_priority: Normal
ms.assetid: cb221974-2f1a-edb0-477b-39a3c4a64c56
description: Y を表す-ローカル座標でのコントロール ハンドルのアンカー ポイントの座標です。 アンカー ポイントは、ダイナミックス機能を使うときのラバーバンディングに使用されます。
ms.openlocfilehash: 162f062d382f3f303ae39db725f3fbfa0790bfc4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806864"
---
# <a name="y-dynamics-cell-controls-section"></a>[Y Dynamics] セル ([コントロール] セクション)

*Y*を表す-ローカル座標でのコントロール ハンドルのアンカー ポイントの座標です。 アンカー ポイントは、ダイナミックス機能を使うときのラバーバンディングに使用されます。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y Dynamics] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | 制御します。  *名*です。YDynwhere を制御します。  *名*は、コントロールの行の名前です。  <br/> |
   
プログラムから、インデックスによって [Y Dynamics] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionControls** <br/> |
| 行インデックス:  <br/> |**visRowControl** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visCtlYDyn** <br/> |
   

