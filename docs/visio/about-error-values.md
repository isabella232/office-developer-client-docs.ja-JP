---
title: エラー値について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251832
localization_priority: Normal
ms.assetid: 56430658-a798-c004-b4ba-363443f43ded
description: エラー値は、誤った数式を含むセルに表示されます。
ms.openlocfilehash: 301f566151362727daf8236f8ca88fca8758054e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804729"
---
# <a name="about-error-values"></a>エラー値について

エラー値は、誤った数式を含むセルに表示されます。
  
数式がエラー値を含むセルを参照すると、その数式にもエラー値が表示されます。ISERR、ISERRNA、ISERROR、または ISERRVALUE 関数を使用してエラー値を検索できます。
  
**エラー値**

||||
|:-----|:-----|:-----|
|**セルに表示される場合** <br/> |**数式が含まれています** <br/> |**例** <br/> |
| #DIV/0!  <br/> |0 で除算しました。  <br/> |10/0  <br/> |
| #VALUE!  <br/> | 引数またはオペランドの型が間違って  <br/> | 5 +「ハウス」  <br/> |
| #REF!  <br/> | 存在しないセルへの参照  <br/> | 存在しない別のセルを参照するセル  <br/> |
| #NUM!  <br/> | 数値は無効です。  <br/> | 負の数値の平方根を求めます  <br/> |
| #N/A!  <br/> | 使用可能な値ではありません。  <br/> | NA () 関数  <br/> |
| #DIM!  <br/> | 寸法の範囲を超える寸法値 (有効な指数は、整数-128 \<n の = \<= 127)  <br/> 不適切な演算で使用される寸法値  <br/> |1 in ^100\*に 1 ^100 (1 の結果は、^200 で、ディメンションの範囲を超えている)  <br/> 5.2 cm ^1.5 (整数乗しません)  <br/> |
   

