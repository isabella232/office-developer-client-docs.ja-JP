---
title: '[Gamma] セル ([Image Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm410
localization_priority: Normal
ms.assetid: 3dcaee26-391c-0494-4380-890ee825dc47
description: モニターやスキャナーなど、特定の出力装置に合わせてイメージの明暗度の強さを調整または補正します。既定値は 1 (補正なし) です。
ms.openlocfilehash: d00eb11ff1feffacf0d758bb25cdd56281e91327
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315205"
---
# <a name="gamma-cell-image-properties-section"></a>[Gamma] セル ([Image Properties] セクション)

モニターやスキャナーなど、特定の出力装置に合わせてイメージの明暗度の強さを調整または補正します。既定値は 1 (補正なし) です。
  
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Gamma] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Gamma  <br/> |
   
プログラムから、インデックスによって [Gamma] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowImage** <br/> |
| セル インデックス:  <br/> |**viシム agegamma** <br/> |
   

