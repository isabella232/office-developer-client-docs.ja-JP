---
title: '[Y Behavior] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1190
localization_priority: Normal
ms.assetid: 6d5062d3-743b-8664-8ec9-5a8f11d5edf9
description: Y の動作の種類を制御・ コントロール ハンドルの座標は、ハンドルを移動した後が発生します。 これらの数式を利用できます。
ms.openlocfilehash: ee2a5e28748df603635f64c080119e28569f576a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806828"
---
# <a name="y-behavior-cell-controls-section"></a>[Y Behavior] セル ([Controls] セクション)

*Y*の動作の種類を制御・ コントロール ハンドルの座標は、ハンドルを移動した後が発生します。 これらの数式を利用できます。 
  
|**値**|**動作**|**定義**|**オートメーション定数**|
|:-----|:-----|:-----|:-----|
| 0  <br/> | 比例  <br/> | コントロール ハンドルを移動することができ、それが伸縮するときは、図形の縦横比にも移動します。  <br/> |**visCtlProportional** <br/> |
| 1  <br/> | プロポーショナル (ロック)  <br/> | コントロール ハンドル、図形では、比例して移動しますが、コントロール ハンドル自体は移動できません。  <br/> |**visCtlLocked** <br/> |
| 2  <br/> | 下端からオフセットします。  <br/> | コントロール ハンドルにオフセット図形の下端から一定の距離です。  <br/> |**visCtlOffsetMin** <br/> |
| 3  <br/> | 中心からオフセットします。  <br/> | コントロール ハンドルにオフセット図形の中心から一定の距離です。  <br/> |**visCtlOffsetMid** <br/> |
| 4  <br/> | 上端からオフセットします。  <br/> | コントロール ハンドルにオフセット図形の上部から一定の距離です。  <br/> |**visCtlOffsetMax** <br/> |
| 5  <br/> | 比例、非表示  <br/> | 0 ですが、コントロール ハンドルと同じが表示されていません。  <br/> |**visCtlProportionalHidden** <br/> |
| 6  <br/> | プロポーショナル ロック、非表示  <br/> | 1 ですが、コントロール ハンドルと同じが表示されていません。  <br/> |**visCtlLockedHiddenv** <br/> |
| 7  <br/> | 非表示、左の端からのオフセットします。  <br/> | 2、ですが、コントロール ハンドルと同じが表示されていません。  <br/> |**visCtlOffsetMinHidden** <br/> |
| 8  <br/> | 非表示にして、中心からオフセットします。  <br/> | 3、ですが、コントロール ハンドルと同じが表示されていません。  <br/> |**visCtlOffsetMidHidden** <br/> |
| 9  <br/> | 非表示、右端からオフセットします。  <br/> | 4 ですが、コントロール ハンドルと同じが表示されていません。  <br/> |**visCtlOffsetMaxHidden** <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Y Behavior] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | 制御します。  *名*です。YConwhere を制御します。  *名*は、コントロールの行の名前です。  <br/> |
   
プログラムから、インデックスによって [Y Behavior] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionControls** <br/> |
| 行インデックス:  <br/> |**visRowControl** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visCtlYCon** <br/> |
   

