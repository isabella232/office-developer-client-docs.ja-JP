---
title: '[SketchAmount] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: スケッチ効果に対するゆがみの量を、0 から 25 の整数で決定します。
ms.openlocfilehash: dc33ea18881cce3d7e5a31f4522074a7b942ddb4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549603"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a>[SketchAmount] セル ([追加効果のプロパティ] セクション)

スケッチ効果に対するゆがみの量を、0 から 25 の整数で決定します。 
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |図形には、適用されるスケッチ効果はありません。  <br/> |
|1-25  <br/> |図形には、スケッチのゆがみが適用されています。1 の値ではゆがみがもっとも大きく、25 ではもっとも小さくなります。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**SketchAmount**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | SketchAmount  <br/> |
   
プログラムから、インデックスによって [**SketchAmount**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visSketchAmount** <br/> |
   

