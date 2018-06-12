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
ms.openlocfilehash: 858d98c8ee55eb49f58bbe98491ddc8752e75504
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805298"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a>[DynFeedback] セル ([Miscellaneous] セクション)

コネクタをドラッグしたときにユーザーに対して表示されるフィードバックの種類を変更します。マウス ボタンを離した後に表示されるコネクタ図形は、この設定の影響を受けません。またこの設定は、経路指定が可能なコネクタには適用されません。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 直線を維持します (脚なし)。  <br/> |**visDynFBDefault** <br/> |
| 1  <br/> | ドラッグすると脚を 3 本表示します。  <br/> |**visDynFBUCon3Leg** <br/> |
| 2  <br/> | ドラッグすると脚を 5 本表示します。  <br/> |**visDynFBUCon5Leg** <br/> |
   
## <a name="remarks"></a>Remarks

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[DynFeedback] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | DynFeedback  <br/> |
   
プログラムから、インデックスによって [DynFeedback] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowMisc** <br/> |
| セル インデックス:  <br/> |**visDynFeedback** <br/> |
   

