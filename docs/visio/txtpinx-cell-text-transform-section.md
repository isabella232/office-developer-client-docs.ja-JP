---
title: '[TxtPinX] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
localization_priority: Normal
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: X を決定するが、テキスト ブロックの図形の原点を基準として回転の中心の座標です。 既定の数式は次のとおりです。
ms.openlocfilehash: df103557d103dbde7e4a1c8d67cabe37a0af9311
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806701"
---
# <a name="txtpinx-cell-text-transform-section"></a>[TxtPinX] セル ([Text Transform] セクション)

*X*の決定に、テキスト ブロックの図形の原点を基準として回転の中心の座標。 既定の数式は次のとおりです。 
  
= 幅\*0.5
  
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [txtpinx] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [Txtpinx]  <br/> |
   
プログラムから、インデックスによって [txtpinx] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowTextXForm** <br/> |
| セル インデックス:  <br/> |**visXFormPinX** <br/> |
   

