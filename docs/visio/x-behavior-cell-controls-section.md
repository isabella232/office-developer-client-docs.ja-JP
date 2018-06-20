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
# <a name="x-behavior-cell-controls-section"></a>[X Behavior] セル ([Controls] セクション)

*X*の動作の種類を制御・ コントロール ハンドルの座標は、ハンドルを移動した後が発生します。 
  
|**値**|**動作**|**定義**|**オートメーション定数**|
|:-----|:-----|:-----|:-----|
| 0  <br/> | 比例  <br/> | コントロール ハンドルを移動することができ、それが伸縮するときは、図形の縦横比にも移動します。  <br/> |**visCtlProportional** <br/> |
| 1  <br/> | プロポーショナル (ロック)  <br/> | コントロール ハンドル、図形に比例して移動しますが、コントロール ハンドル自体は移動できません。  <br/> |**visCtlLocked** <br/> |
| 2  <br/> | 左端からのオフセットします。  <br/> | コントロール ハンドルにオフセット図形の左端から一定の距離です。  <br/> |**visCtlOffsetMin** <br/> |
| 3  <br/> | 中心からオフセットします。  <br/> | コントロール ハンドルにオフセット図形の中心から一定の距離です。  <br/> |**visCtlOffsetMid** <br/> |
| 4  <br/> | 右端からオフセットします。  <br/> | コントロール ハンドルにオフセット図形の右側から一定の距離です。  <br/> |**visCtlOffsetMax** <br/> |
| 5  <br/> | 比例、非表示  <br/> | 0 ですが、コントロール ハンドルと同じが表示されていません。  <br/> |**visCtlProportionalHidden** <br/> |
| 6  <br/> | プロポーショナル ロック、非表示  <br/> | 1 ですが、コントロール ハンドルと同じが表示されていません。  <br/> |**visCtlLockedHiddenv** <br/> |
| 7  <br/> | 非表示、左の端からのオフセットします。  <br/> | 2、ですが、コントロール ハンドルと同じが表示されていません。  <br/> |**visCtlOffsetMinHidden** <br/> |
| 8  <br/> | 非表示にして、中心からオフセットします。  <br/> | 3、ですが、コントロール ハンドルと同じが表示されていません。  <br/> |**visCtlOffsetMidHidden** <br/> |
| 9  <br/> | 非表示、右端からオフセットします。  <br/> | 4 ですが、コントロール ハンドルと同じが表示されていません。  <br/> |**visCtlOffsetMaxHidden** <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[X Behavior] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | 制御します。  *名*です。XConwhere を制御します。  *名*は、コントロールの行の名前です。  <br/> |
   
プログラムから、インデックスによって [X Behavior] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionControls** <br/> |
| 行インデックス:  <br/> |**visRowControl** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visCtlXCon** <br/> |
   

