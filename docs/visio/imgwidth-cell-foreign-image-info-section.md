---
title: '[ImgWidth] セル ([Foreign Image Info] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm460
localization_priority: Normal
ms.assetid: b57fb962-0b3e-f2e5-3b88-3edf33e40496
description: 枠内におけるオブジェクトのイメージの幅を指定します。既定の数式は次のとおりです。
ms.openlocfilehash: 3aab65d27d426287060f7572dad15174acb93199
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805572"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a>[ImgWidth] セル ([Foreign Image Info] セクション)

枠内におけるオブジェクトのイメージの幅を指定します。既定の数式は次のとおりです。
  
= 幅\*1
  
オブジェクトをトリミングすると、Width に掛ける係数が変化します。
  
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [imgwidth] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [Imgwidth]  <br/> |
   
プログラムから、インデックスによって [imgwidth] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowForeign** <br/> |
| セル インデックス:  <br/> |**visFrgnImgWidth** <br/> |
   

