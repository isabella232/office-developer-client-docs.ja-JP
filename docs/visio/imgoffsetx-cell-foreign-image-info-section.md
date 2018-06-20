---
title: '[ImgOffsetX] セル ([Foreign Image Info] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251308
localization_priority: Normal
ms.assetid: c079fb10-4db7-4657-75d2-2fb953c86670
description: オブジェクトの距離は、オブジェクトの枠の原点から水平方向にオフセットを決定します。 既定値は 0 です。 トリミング ツールの変更をオブジェクトにこの値をパンします。
ms.openlocfilehash: dda385b2157e48baec2b21c6da741b31d05c3291
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805573"
---
# <a name="imgoffsetx-cell-foreign-image-info-section"></a>[ImgOffsetX] セル ([Foreign Image Info] セクション)

オブジェクトの距離は、オブジェクトの枠の原点から水平方向にオフセットを決定します。 既定値は 0 です。 **トリミング**ツールの変更をオブジェクトにこの値をパンします。 
  
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ImgOffsetX] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ImgOffsetX  <br/> |
   
プログラムから、インデックスによって [ImgOffsetX] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowForeign** <br/> |
| セル インデックス:  <br/> |**visFrgnImgOffsetX** <br/> |
   

