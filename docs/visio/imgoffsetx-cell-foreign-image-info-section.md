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
description: オブジェクトの枠の原点からオブジェクトを水平方向へオフセットする距離を指定します。 既定値は 0 です。 [トリミング ツール] を使用してオブジェクトをパンすると、この値が変化します。
ms.openlocfilehash: d9b3e97a07bc1cadc0276905c4199861ab0590ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335407"
---
# <a name="imgoffsetx-cell-foreign-image-info-section"></a>[ImgOffsetX] セル ([Foreign Image Info] セクション)

オブジェクトの枠の原点からオブジェクトを水平方向へオフセットする距離を指定します。既定値は 0 です。**[トリミング ツール]** を使用してオブジェクトをパンすると、この値が変化します。 
  
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ImgOffsetX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [imgoffsetx]  <br/> |
   
プログラムから、インデックスによって [ImgOffsetX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowForeign** <br/> |
| セル インデックス:  <br/> |**visFrgnImgOffsetX** <br/> |
   

