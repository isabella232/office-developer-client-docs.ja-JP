---
title: '[RotateGradientWithShape] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: 塗りつぶしのグラデーションが 2D 回転で図形に合わせて回転するかどうかを、ブール演算型で決定します。
ms.openlocfilehash: 76a76a4a97128c81710269f75e9e17db90827377
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412220"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a>[RotateGradientWithShape] セル ([グラデーションのプロパティ] セクション)

塗りつぶしのグラデーションが 2D 回転で図形に合わせて回転するかどうかを、ブール演算型で決定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |図形が回転ピンを中心に回転するとき、グラデーションは図形に合わせて回転します。 グラデーションの "上部" は、回転ハンドルに対して平行です。  <br/> |
|FALSE  <br/> |図形が回転ピンを中心に回転するとき、グラデーションは図形に合せて回転しません。 グラデーションの "上部" は、描画キャンバスに対して平行です。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**RotateGradientWithShape**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [rotategradientwithshape]  <br/> |
   
プログラムから、インデックスによって [**RotateGradientWithShape**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowGradientProperties** <br/> |
| セル インデックス:  <br/> |**visRotateGradientWithShape** <br/> |
   

