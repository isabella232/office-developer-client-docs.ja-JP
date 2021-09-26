---
title: '[Y Behavior] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1190
ms.localizationpriority: medium
ms.assetid: 6d5062d3-743b-8664-8ec9-5a8f11d5edf9
description: ハンドルの移動後にコントロール ハンドルの y 座標が表示される動作の種類を制御します。 次の数式を使用できます。
ms.openlocfilehash: 6f24533f0354b84f10e9409e9c1af64d55aab6ec
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612450"
---
# <a name="y-behavior-cell-controls-section"></a>[Y Behavior] セル ([Controls] セクション)

ハンドルの移動後に  *コントロール ハンドルの y*  座標が表示される動作の種類を制御します。 次の数式を使用できます。 
  
|**値**|**動作**|**定義**|**オートメーション定数**|
|:-----|:-----|:-----|:-----|
| 0  <br/> | プロポーショナル  <br/> |  
          コントロール ハンドルを移動できます。また図形を引き伸ばすと、図形に比例して移動します。
          <br/> |**visCtlProportional** <br/> |
| 1  <br/> | プロポーショナル (ロック)  <br/> | コントロール ハンドルは図形に比例して移動しますが、コントロール ハンドル自体は移動できません。  <br/> |**visCtlLocked** <br/> |
| 2  <br/> | 下端からオフセット  <br/> | コントロール ハンドルは、図形の底部から一定の距離だけオフセットされます。  <br/> |**visCtlOffsetMin** <br/> |
| 3  <br/> | 中心からオフセット  <br/> | コントロール ハンドルは、図形の中心から一定の距離だけオフセットされます。  <br/> |**visCtlOffsetMid** <br/> |
| 4   <br/> | 上端からオフセット  <br/> | コントロール ハンドルは、図形の上部から一定の距離だけオフセットされます。  <br/> |**visCtlOffsetMax** <br/> |
| 5  <br/> | プロポーショナル (非表示)  <br/> | 0 と同じですが、コントロール ハンドルは表示されません。  <br/> |**visCtlProportionalHidden** <br/> |
| 6   <br/> | プロポーショナル (ロック、非表示)  <br/> | 1 と同じですが、コントロール ハンドルは表示されません。  <br/> |**visCtlLockedHiddenv** <br/> |
| 7   <br/> | 左端からオフセット (非表示)  <br/> | 2 と同じですが、コントロール ハンドルは表示されません。  <br/> |**visCtlOffsetMinHidden** <br/> |
| 8   <br/> | 中心からオフセット (非表示)  <br/> | 3 と同じですが、コントロール ハンドルは表示されません。  <br/> |**visCtlOffsetMidHidden** <br/> |
| 9   <br/> | 右端からオフセット (非表示)  <br/> | 4 と同じですが、コントロール ハンドルは表示されません。  <br/> |**visCtlOffsetMaxHidden** <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y Behavior] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | コントロール。  *name*  .YConwhere コントロール。  *name*  は、コントロール行の名前です。  <br/> |
   
プログラムから、インデックスによって [Y Behavior] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionControls** <br/> |
| 行インデックス:  <br/> |**visRowControl**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visCtlYCon** <br/> |
   

