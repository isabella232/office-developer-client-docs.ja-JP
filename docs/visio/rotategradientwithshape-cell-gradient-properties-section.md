---
title: '[RotateGradientWithShape] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: 塗りつぶしのグラデーションが 2D 回転で図形に合わせて回転するかどうかを、ブール演算型で決定します。
ms.openlocfilehash: d752f870fd08c1a47dfc7ce193b6976a1bdb2a1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806242"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a>[RotateGradientWithShape] セル ([グラデーションのプロパティ] セクション)

塗りつぶしのグラデーションが 2D 回転で図形に合わせて回転するかどうかを、ブール演算型で決定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |グラデーションは、周りの回転の暗証番号 (pin)、図形を回転させて、図形を回転します。 グラデーションの「上」は、回転ハンドルに平行です。  <br/> |
|FALSE  <br/> |回転の暗証番号 (pin) を中心に図形を回転すると、グラデーションは図形を回転しません。 グラデーションの「上」は、描画キャンバスに平行です。  <br/> |
   
## <a name="remarks"></a>備考

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **RotateGradientWithShape** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | RotateGradientWithShape  <br/> |
   
プログラムから、インデックスによって [ **RotateGradientWithShape** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowGradientProperties** <br/> |
| セル インデックス:  <br/> |**visRotateGradientWithShape** <br/> |
   

