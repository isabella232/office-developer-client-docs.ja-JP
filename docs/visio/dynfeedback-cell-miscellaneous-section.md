---
title: '[DynFeedback] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251317
localization_priority: Normal
ms.assetid: 44017319-7146-3431-e476-fbb1a40341ca
description: コネクタをドラッグしたときにユーザーに対して表示されるフィードバックの種類を変更します。マウス ボタンを離した後に表示されるコネクタ図形は、この設定の影響を受けません。またこの設定は、経路指定が可能なコネクタには適用されません。
ms.openlocfilehash: 823b8db4dc6afe94a5fdac1f62aaa48d7e1b0d80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315744"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a>[DynFeedback] セル ([Miscellaneous] セクション)

コネクタをドラッグしたときにユーザーに対して表示されるフィードバックの種類を変更します。マウス ボタンを離した後に表示されるコネクタ図形は、この設定の影響を受けません。またこの設定は、経路指定が可能なコネクタには適用されません。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| .0  <br/> | 直線を維持します (脚なし)。  <br/> |**visDynFBDefault** <br/> |
| 1-d  <br/> | ドラッグすると脚を 3 本表示します。  <br/> |**visDynFBUCon3Leg** <br/> |
| pbm-2  <br/> | ドラッグすると脚を 5 本表示します。  <br/> |**visDynFBUCon5Leg** <br/> |
   
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DynFeedback] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [dynfeedback]  <br/> |
   
プログラムから、インデックスによって [DynFeedback] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowMisc** <br/> |
| セル インデックス:  <br/> |**visDynFeedback** <br/> |
   

