---
title: '[DistanceFromGround] セル ([3-D 回転のプロパティ)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87499dab-977a-45bc-9f6a-8daa80a82abb
description: オブジェクトに 3-D の回転時に地面から発生する距離を指定します。
ms.openlocfilehash: da544d0340c0fca0103c147f27b715784643153f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805216"
---
# <a name="distancefromground-cell-3-d-rotation-properties"></a>[DistanceFromGround] セル ([3-D 回転のプロパティ)

オブジェクトに 3-D の回転時に地面から発生する距離を指定します。
  
## <a name="remarks"></a>備考

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **DistanceFromGround** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |DistanceFromGround  <br/> |
   
プログラムから、インデックスによって [ **DistanceFromGround** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRow3DRotationProperties** <br/> |
|セル インデックス:  <br/> |**visDistanceFromGround** <br/> |
   

