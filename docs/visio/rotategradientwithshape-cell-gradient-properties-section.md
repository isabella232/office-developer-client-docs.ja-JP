---
title: '[RotateGradientWithShape] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: 塗りつぶしのグラデーションが 2D 回転で図形に合わせて回転するかどうかを、ブール演算型で決定します。
ms.openlocfilehash: ac3f5bee458a20f94539f3c2077286c6bb4b3b56
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570163"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a>[RotateGradientWithShape] セル ([グラデーションのプロパティ] セクション)

塗りつぶしのグラデーションが 2D 回転で図形に合わせて回転するかどうかを、ブール演算型で決定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |図形が回転ピンを中心に回転するとき、グラデーションは図形に合わせて回転します。 グラデーションの "上" は回転ハンドルと平行です。  <br/> |
|FALSE  <br/> |図形が回転ピンを中心に回転するとき、グラデーションは図形に合せて回転しません。 グラデーションの "上" は描画キャンバスと平行です。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**RotateGradientWithShape**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | RotateGradientWithShape  <br/> |
   
プログラムから、インデックスによって [**RotateGradientWithShape**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowGradientProperties** <br/> |
| セル インデックス:  <br/> |**visRotateGradientWithShape** <br/> |
   

