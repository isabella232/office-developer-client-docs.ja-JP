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
description: ハンドルを移動したときにコントロールハンドルの y 座標が示す動作の種類を制御します。 次の数式を使用できます。
ms.openlocfilehash: bf8cbd490884244c92b68784dcbf041093539c94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360145"
---
# <a name="y-behavior-cell-controls-section"></a>[Y Behavior] セル ([Controls] セクション)

ハンドルを移動したときにコントロールハンドルの*y*座標が示す動作の種類を制御します。 次の数式を使用できます。 
  
|**値**|**Behavior**|**定義**|**オートメーション定数**|
|:-----|:-----|:-----|:-----|
| .0  <br/> | 正比例  <br/> |  
          コントロール ハンドルを移動できます。また図形を引き伸ばすと、図形に比例して移動します。
          <br/> |**visctlproportional** <br/> |
| 1-d  <br/> | プロポーショナル (ロック)  <br/> | コントロール ハンドルは図形に比例して移動しますが、コントロール ハンドル自体は移動できません。  <br/> |**visctllocked** <br/> |
| pbm-2  <br/> | 下端からオフセット  <br/> | コントロール ハンドルは、図形の底部から一定の距離だけオフセットされます。  <br/> |**visctloffsetmin** <br/> |
| 1/3  <br/> | 中心からオフセット  <br/> | コントロール ハンドルは、図形の中心から一定の距離だけオフセットされます。  <br/> |**visctloffsetmid** <br/> |
| 2/4  <br/> | 上端からオフセット  <br/> | コントロール ハンドルは、図形の上部から一定の距離だけオフセットされます。  <br/> |**visctloffsetmax** <br/> |
| 5  <br/> | プロポーショナル (非表示)  <br/> | 0 と同じですが、コントロール ハンドルは表示されません。  <br/> |**visCtlProportionalHidden** <br/> |
| シックス  <br/> | プロポーショナル (ロック、非表示)  <br/> | 1 と同じですが、コントロール ハンドルは表示されません。  <br/> |**visCtlLockedHiddenv** <br/> |
| 7  <br/> | 左端からオフセット (非表示)  <br/> | 2 と同じですが、コントロール ハンドルは表示されません。  <br/> |**visctloffsetminhidden** <br/> |
| ~  <br/> | 中心からオフセット (非表示)  <br/> | 3 と同じですが、コントロール ハンドルは表示されません。  <br/> |**visctloffsetmidhidden** <br/> |
| i-9  <br/> | 右端からオフセット (非表示)  <br/> | 4 と同じですが、コントロール ハンドルは表示されません。  <br/> |**visCtlOffsetMaxHidden** <br/> |
   
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y Behavior] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | 管理.  *名前*です。yconwhere  *name*は、コントロール行の名前です。  <br/> |
   
プログラムから、インデックスによって [Y Behavior] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionControls** <br/> |
| 行インデックス:  <br/> |**visRowControl** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visc・ con** <br/> |
   

