---
title: '[X Behavior] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251285
localization_priority: Normal
ms.assetid: 82423d08-b6ce-0f23-8b61-354c3e5f323e
description: X の動作の種類を制御・ コントロール ハンドルの座標は、ハンドルを移動した後が発生します。
ms.openlocfilehash: 004ad407941aa15cec3ae94188f590ec6513c4da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806802"
---
# <a name="x-behavior-cell-controls-section"></a>[X Behavior] セル ([コントロール] セクション)

*X*の動作の種類を制御・ コントロール ハンドルの座標は、ハンドルを移動した後が発生します。 
  
|**値**|**動作**|**定義**|**オートメーション定数**|
|:-----|:-----|:-----|:-----|
| 0  <br/> |  
          プロポーショナル 
          <br/> |  
          コントロール ハンドルを移動できます。また図形を引き伸ばすと、図形に比例して移動します。
          <br/> |**visCtlProportional** <br/> |
| 1  <br/> |  
          プロポーショナル (ロック) 
          <br/> |  
          コントロール ハンドルは図形に比例して移動しますが、コントロール ハンドル自体は移動できません。 
          <br/> |**visCtlLocked** <br/> |
| 2  <br/> |  
          左端からオフセット 
          <br/> |  
          コントロール ハンドルは、図形の左辺から一定の距離だけオフセットされます。 
          <br/> |**visCtlOffsetMin** <br/> |
| 3  <br/> |  
          中心からオフセット 
          <br/> |  
          コントロール ハンドルは、図形の中心から一定の距離だけオフセットされます。
          <br/> |**visCtlOffsetMid** <br/> |
| 4  <br/> |  
          右端からオフセット 
          <br/> |  
          コントロール ハンドルは、図形の右辺から一定の距離だけオフセットされます。 
          <br/> |**visCtlOffsetMax** <br/> |
| 5  <br/> |  
          プロポーショナル (非表示) 
          <br/> |  
          0 と同じですが、コントロール ハンドルは表示されません。 
          <br/> |**visCtlProportionalHidden** <br/> |
| 6  <br/> |  
          プロポーショナル (ロック、非表示) 
          <br/> |  
          1 と同じですが、コントロール ハンドルは表示されません。 
          <br/> |**visCtlLockedHiddenv** <br/> |
| 7  <br/> |  
          左端からオフセット (非表示) 
          <br/> |  
          2 と同じですが、コントロール ハンドルは表示されません。 
          <br/> |**visCtlOffsetMinHidden** <br/> |
| 8  <br/> |  
          中心からオフセット (非表示) 
          <br/> |  
          3 と同じですが、コントロール ハンドルは表示されません。 
          <br/> |**visCtlOffsetMidHidden** <br/> |
| 9  <br/> |  
          右端からオフセット (非表示) 
          <br/> |  
          4 と同じですが、コントロール ハンドルは表示されません。 
          <br/> |**visCtlOffsetMaxHidden** <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X Behavior] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | 制御します。  *名*です。XConwhere を制御します。  *名*は、コントロールの行の名前です。  <br/> |
   
プログラムから、インデックスによって [X Behavior] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionControls** <br/> |
| 行インデックス:  <br/> |**visRowControl** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visCtlXCon** <br/> |
   

